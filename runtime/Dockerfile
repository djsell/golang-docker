FROM google/golang

RUN go get github.com/tools/godep
ADD go-build /bin/go-build
ADD go-run /bin/go-run

ONBUILD ADD . /gopath/src/app/
ONBUILD RUN /bin/go-build

ENTRYPOINT ["/bin/go-run"]
