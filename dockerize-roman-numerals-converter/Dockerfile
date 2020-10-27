FROM ubuntu
RUN apt-get update -y && \
    apt-get install -y python3-pip python3 git
WORKDIR /app
RUN git clone https://github.com/gulec2000/Clarusway-Aws-DevOps-Workshop.git && \
    mv Clarusway-Aws-DevOps-Workshop/aws/projects/001-roman-numerals-converter/* . && \
    rm -rf Clarusway-Aws-DevOps-Workshop && \
    apt-get remove -y git
COPY requirements.txt .
RUN pip3 install -r requirements.txt
EXPOSE 80
ENTRYPOINT ["python3"]
CMD ["app.py"]