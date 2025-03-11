# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 as base

RUN mkdir -p /compilers/android/ndk-r27c

RUN wget -O android-ndk-r27c-linux.zip "https://dl.google.com/android/repository/android-ndk-r27c-linux.zip"
RUN unzip android-ndk-r27c-linux.zip -d /compilers/android/ndk-r27c

# we only need the clang-x.y.z binary

RUN mv -f /compilers/android/ndk-r27c/android-ndk-r27c/toolchains/llvm/prebuilt/linux-x86_64/* /compilers/android/ndk-r27c/

RUN rm -rf /compilers/android/ndk-r27c/android-ndk-r27c

RUN rm -rf /compilers/android/ndk-r27c/libexec
RUN rm -rf /compilers/android/ndk-r27c/share
RUN rm -rf /compilers/android/ndk-r27c/prebuilt_include
RUN rm -rf /compilers/android/ndk-r27c/*.txt
RUN rm -rf /compilers/android/ndk-r27c/*.md
RUN rm -rf /compilers/android/ndk-r27c/*.xml
RUN rm -rf /compilers/android/ndk-r27c/BUILD_INFO
RUN rm -rf /compilers/android/ndk-r27c/NOTICE
RUN rm -rf /compilers/android/ndk-r27c/MODULE_*
RUN rm -rf /compilers/android/ndk-r27c/sysroot/NOTICE

RUN chown -R root:root /compilers/android/ndk-r27c/
RUN chmod +x /compilers/android/ndk-r27c/bin/*

FROM scratch as release

COPY --from=base /compilers /compilers
