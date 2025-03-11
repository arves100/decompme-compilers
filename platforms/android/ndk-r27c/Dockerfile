# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/android/ndk-r27c

RUN wget -O android-ndk-r27c-linux.zip "https://dl.google.com/android/repository/android-ndk-r27c-linux.zip"
RUN unzip android-ndk-r27c-linux.zip -d /compilers/android/ndk-r27c

RUN chown -R root:root /compilers/android/ndk-r27c/
RUN chmod +x /compilers/android/ndk-r27c/*


FROM scratch as release

COPY --from=base /compilers /compilers
