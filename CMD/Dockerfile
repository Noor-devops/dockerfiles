FROM almalinux:9
RUN dnf install nginx -y
LABEL author="sivakumar" \
      course="docker" \
      duration="10hrs"
EXPOSE 80
ENV course="docker" \
    trainer="sivakumar" \
    duration="10hrs"
CMD ["nginx", "-g", "daemon off;"]