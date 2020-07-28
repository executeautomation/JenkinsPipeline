FROM jenkins/slave:latest-jdk11

USER root

RUN apt-get update && apt-get install -y maven

RUN set -eux; \
	apt-get update; \
	apt-get install -y --no-install-recommends \
		bzip2 \
		unzip \
		xz-utils

RUN usermod -a -G root jenkins

# Good idea to switch back to the jenkins user.
USER jenkins