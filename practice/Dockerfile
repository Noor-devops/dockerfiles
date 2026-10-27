ARG version
FROM almalinux:${version:-9}
WORKDIR /app
RUN useradd roboshop \
    && dnf install nginx -y \
    && dnf clean all
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
COPY html/ /usr/share/nginx/html/
#ONBUILD COPY html/index.html /usr/share/nginx/html/
#ENTRYPOINT ["nginx"]
#USER roboshop
CMD [ "nginx", "-g", "daemon off;" ]