FROM vauxoo/odoo-80-image
MAINTAINER Tulio Ruiz <tulio@vauxoo.com>

ENV RUN_COMMAND_MQT_10_ENTRYPOINT_IMAGE="/entrypoint_image" \
    INSTANCE_ALIVE="1" PSQL_VERSION="9.3" \
    REPO_REQUIREMENTS="/.repo_requirements" \
    WITHOUT_DEPENDENCIES="1" OCA_RUNBOT="1"

COPY scripts/entrypoint_image /
COPY scripts/*.sh /usr/share/vx-docker-internal/odoo-shippable/
RUN bash /usr/share/vx-docker-internal/odoo-shippable/build-image.sh

EXPOSE 5432 8069 8070 8071 8072 22 60000-60005/udp
