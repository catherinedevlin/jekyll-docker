FROM ubuntu:utopic
MAINTAINER Jekyll Core <hello@jekyllrb.com>
ENV RUBY_SHA=5a4de38068eca8919cb087d338c0c2e3d72c9382c804fb27ab746e6c7819ab28
ENV DEBCONF_FRONTEND=noninteractive
ENV PATH=${PATH}:/opt/jekyll/bin
ENV JEKYLL_VERSION=2.5.3
ENV RUBY_VERSION=2.2.1

COPY copy/ /
RUN useradd -m -s /bin/bash jekyll
RUN echo "debconf debconf/frontend select Noninteractive" | debconf-set-selections
RUN bash /usr/share/jekyll/setup.bash
WORKDIR /srv/jekyll
EXPOSE 4000
USER jekyll
