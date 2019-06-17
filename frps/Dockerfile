FROM alpine as build
WORKDIR /tmp
ADD https://github.com/fatedier/frp/releases/download/v0.27.0/frp_0.27.0_linux_amd64.tar.gz .
RUN tar -zxvf frp_0.27.0_linux_amd64.tar.gz

FROM alpine as final
COPY --from=build /tmp/frp_0.27.0_linux_amd64/frps /usr/bin
COPY --from=build /tmp/frp_0.27.0_linux_amd64/frps.ini /etc/frps/frps.ini
ENTRYPOINT [ "frpc","-c","/etc/frps/frps.ini" ]