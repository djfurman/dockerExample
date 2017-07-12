# Docker Example

Taken directly from the docker getting started documents, this project leverages the python3.6 official distribution based on Alpine Linux to establish a simple Flask application.

## Purpose

Display a simple webpage running Flask within docker on your local machine.

## Usage

    1. Install Docker
    2. Clone this repository
    3. Execute `docker build -t dansayshello .`, this builds the docker image and tags it as 'dansayshello'
    4. Execute `docker run -p 8000:80 dansayshello`
    5. Navigate to http://localhost:8000
    6. Kill the container with `ctrl + c` 

### Extra Credit/Help

You can also run `docker ps` to identify the instance name and kill manually if you're an advanced user and deamonized the instances. Props to you if did so, but you're outside the scope of why this repo was constructed, I just didn't want you stuck rebooting to get out of it.

## What does that do?

By using the build command, docker will essentially compile a working container for usage; the run command executes it, while the `-p` flag forwards a local port to the web port on the docker image now running.

## Why Apline?

Before getting started in the Docker community I'd never worked with Alpine Linux, and I'm happy to say that I'm extremely pleased with the experience so far. Alpine is build for the containerized world. It is a powerful, secure, but no-overhead distribution that makes it ideal to run micro-services within contianerization engines like docker.

## Why Docker?

The prevelence of cloud technology is undeniable today, and in order to get the most return on investment, it's important to think of cloud machines as multi purpose hosts. However, in doing so, one must spend a significant amount of time learning security practices to keep applications running under appropriate users, contexts, etc. While docker is not a magic bullet, it makes it much easier to segregate applications and contain them directly.

### Public Service Announcement

I've seen multiple docker instances in the public claim that docker solves security so hard coding credientials (e.g., mysql root password) isn't an issue. This couldn't be further from the truth and my repositories will never include such nonsense. Containers provide security from other apps on the same host, not malicious users. Please ensure that regardless of containeriation solutions that one ALWAYS follows security best practices. If one finds oneself struggling with secrets management in docker apps, please don't hesitate to reach out to me on Twitter, GitHub, LinkedIn, Skype or Email. There are easy solutions I'm happy to share. :)
