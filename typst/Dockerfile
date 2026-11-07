FROM alpine:edge

RUN apk add --no-cache bash curl typst

RUN curl --proto '=https' --tlsv1.2 -LsSf \
    https://github.com/Myriad-Dreamin/tinymist/releases/latest/download/tinymist-installer.sh \
    | sh

ENV PATH="/root/.local/bin:$PATH"