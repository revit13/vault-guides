# Copyright 2020 IBM Corp.
# SPDX-License-Identifier: Apache-2.0

FROM registry.access.redhat.com/ubi8/ubi-minimal
RUN microdnf update -y

WORKDIR /
COPY vault-plugin-secrets-mock .
RUN setcap cap_ipc_lock=+ep $(readlink -f /vault-plugin-secrets-mock)
