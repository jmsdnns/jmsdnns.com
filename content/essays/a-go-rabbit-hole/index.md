---
title: A Go Rabbit Hole
published_at: July 25, 2014 2:05 AM
updated_at: July 25, 2014 2:05 AM
---

I am coming up from a rabbit hole. This is the story of how I went down it in the first place.

Since February, I have been doing Objective-C exclusively. It took a while to learn, but once I got the hang of it I got curious about how people build servers lately. I had spent a lot of time with Python but was feeling bored with it. I figured I'd learn Go.

## Go

I read [Effective Go](https://golang.org/doc/effective_go.html), watched a few talks, and then I started writing code. I put together a basic web system. I spawned some goroutines that communicate with channels. It was both fun and straight-forward and hard concepts appear to have been made significantly easier.

I then wrote some web serving code. Go actually comes with the basic pieces of a web framework built in, even up to the template rendering. I wrote a few web handlers, one that writes JSON, and I used the Osin package to build the basics of an OAuth provider.

Overall, I was surprised by how straight forward it was to put all these ideas together. That seems to be what Go is about, being straight forward and easy to understand. Consider that the designers are [Rob Pike](https://en.wikipedia.org/wiki/Rob_Pike) and [Ken Thompson](https://en.wikipedia.org/wiki/Ken_Thompson), once of Bell Labs, now of Google. They've been at it a long time.

VHX, where I write Objective-C, does tech talks every Wednesday. I spoke about Go at the last one and finished the talk by talking about what kind of things were already written in Go. I wasn't building systems last year, but I remembered people talking about Docker and I remembered people saying it was written in Go, so I mentioned it. My friends in the devops world, who didn't care that it was written in Go, thought the tool was pretty cool too.

I also realized I didn't know anything about Docker.

## Docker

First thing to know about [Docker](https://docker.com/) is that it's a way to create file systems composed of layers. This system is called [UnionFS](https://en.wikipedia.org/wiki/UnionFS). You can take some Ubuntu system and create a container where you layer a few things together to build a service, like a postgres service that depends on a few c libraries, or an nginx service that wants libevent. You could install one version of some library in one container, install a different, incompatible version in another container, and they don't interfere with each other.

In short: UnionFS is a tool for layering file systems and Docker is a way of using UnionFS to run processes.

It seemed like they want to be a thing larger than package managers but smaller than running a complete OS. It works by containing just the file system, after all. Instead of virtualization, which lets mac users run linux (eg. Vagrant), it runs processes inside the host OS. Linux inside Linux works, but not Linux inside OSX. But, you could run a Centos Linux container inside Ubuntu Linux, which is pretty interesting.

I then wondered, if this is a replacement for package managers, could you build an OS out of this?

## CoreOS

That's when I found [CoreOS](https://coreos.com/). It is a minimal Linux, derived from ChromeOS (uh.. wut?), that replaces package management with Docker. It also has the goal of being designed for clusters. Oh, and it's also backed by YC and A16Z.

Uh...?! Seriously? Amazing!

CoreOS attempts to handle clusters by providing a tool called [Fleet](https://github.com/coreos/fleet). Fleet lets you distribute system configurations and control the operation of services in you network. You submit a service file that describes how to create a docker container and turn on/off the service. These services are controlled by [Systemd](http://www.freedesktop.org/wiki/Software/systemd/). [Etcd](https://github.com/coreos/etcd) is where the cluster's configuration is stored. `fleetctl`, the command line tool for fleet, is basically an interface to both Systemd and Etcd.

## Last Few Weeks

I started hacking on Go over July 4th and absorbed the rest between then and now. I have now run a cluster of CoreOS vm's in Vagrant and spent today working with CoreOS inside AWS. It all started because I got curious what Go programmers were up to. Well... turns out they've done an enormous amount of stuff. All of that, except for systemd, is in Go.

So, yeah... I went down a pretty serious rabbit hole and it was awesome.
