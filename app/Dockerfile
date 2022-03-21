# set base image (host OS)
FROM python:latest
RUN pip install --upgrade pip

# set the working directory in the container
RUN adduser worker
USER worker
WORKDIR /home/worker

COPY --chown=worker:worker requirements.txt requirements.txt
RUN pip install --user -r requirements.txt
# copy the dependencies file to the working directory
ENV PATH="/home/worker/.local/bin:${PATH}"

COPY --chown=worker:worker worker/ .
# command to run on container start
CMD [ "python", "./server.py" ]
