FROM unicon/shibboleth-idp:latest

ARG custom_acs_dns_prefix
ARG custom_acs_rdc_location

MAINTAINER Unicon, Inc.

COPY shibboleth-idp/ /opt/shibboleth-idp/

RUN sed -i 's/CUSTOM_ACS_DNS_PREFIX/'"$custom_acs_dns_prefix"'/g' /opt/shibboleth-idp/conf/idp.properties
RUN sed -i 's/CUSTOM_ACS_RDC_LOCATION/'"$custom_acs_rdc_location"'/g' /opt/shibboleth-idp/conf/idp.properties

RUN sed -i 's/CUSTOM_ACS_DNS_PREFIX/'"$custom_acs_dns_prefix"'/g' /opt/shibboleth-idp/metadata/idp-metadata.xml
RUN sed -i 's/CUSTOM_ACS_RDC_LOCATION/'"$custom_acs_rdc_location"'/g' /opt/shibboleth-idp/metadata/idp-metadata.xml
