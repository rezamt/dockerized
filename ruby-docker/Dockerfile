FROM ubuntu

# Updat Ubuntu Repos
RUN apt-get update

# Installing OpenSSL, curl
RUN apt-get install -y openssl curl gcc make g++ build-essential libc6-dev tcl git supervisor

# Creating usr/local for bindin Ruby binaries
RUN mkdir -p /usr/local

RUN curl -L https://cache.ruby-lang.org/pub/ruby/2.4/ruby-2.4.2.tar.gz > /ruby-2.4.2.tar.gz \
       && tar xfz /ruby-2.4.2.tar.gz  -C /
RUN cd /ruby-2.4.2 && ./configure && make && make install
RUN ruby --version
RUN gem --version

