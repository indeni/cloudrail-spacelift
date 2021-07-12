FROM public.ecr.aws/spacelift/runner-terraform:latest as spacelift

# There's no pip/python in the Spacelift image
USER root
RUN apk update \
  && apk add py3-pip bash vim less

# Install Cloudrail and clean up after
RUN umask 022
RUN pip install cloudrail
RUN pip cache purge
