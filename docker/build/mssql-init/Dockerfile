# escape=`

ARG PARENT_IMAGE
ARG HEADLESS_SERVICES_IMAGE
ARG SPE_IMAGE

FROM ${SPE_IMAGE} as spe
FROM ${HEADLESS_SERVICES_IMAGE} AS headless_services
FROM ${PARENT_IMAGE}


# Copy and init the JSS / Headless Services Module
COPY --from=headless_services C:\module\db C:\resources\jss

# copy pse
COPY --from=spe C:\module\db C:\resources\spe
