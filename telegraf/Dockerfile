ARG TELEGRAF_VERSION
FROM telegraf:${TELEGRAF_VERSION}

COPY ./entrypoint-hook.sh /entrypoint-hook.sh
RUN chmod +x /entrypoint-hook.sh

ENTRYPOINT ["/entrypoint-hook.sh"]
CMD ["telegraf", "--config", "/etc/telegraf/config/telegraf.conf", "--config-directory", "/etc/telegraf/config/conf.d"]