ARG version
FROM almalinux:${version:-9}
RUN mkdir /app
WORKDIR /app
RUN useradd roboshop
RUN dnf install nginx -y 
RUN dnf enable nginx -y
RUN dnf start nginx -y
LABEL author="Noor Shanu" \
      course="docker" \
      duration="10hrs"
EXPOSE 80
ARG course="Devops" \
    trainer="Noor Shanu" \
    duration="10hrs"
ENV course=${course} \
    duration=${duration} \
    trainer=${trainer}
COPY index.html /usr/share/nginx/html/index.html
ONBUILD COPY index.html /usr/share/nginx/html/
ENTRYPOINT ["nginx", "-g", "daemon off;"]
USER roboshop
CMD [sleep 1000]