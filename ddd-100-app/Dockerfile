# 基础镜像
FROM openjdk:8-jre-slim

# 作者
MAINTAINER xiaofuge

# 配置
ENV PARAMS=""

# 时区
ENV TZ=PRC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# 添加应用
ADD target/ddd-100-app.jar /ddd-100-app.jar

ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /ddd-100-app.jar $PARAMS"]