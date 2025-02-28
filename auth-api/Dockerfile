FROM golang:1.21.1

# Set destination for COPY
WORKDIR /app

# Download Go modules
COPY go.mod go.sum ./
RUN go mod download

#Copy the source code
COPY *.go ./

#Build
RUN CGO_ENABLED=0 GOOS=linux go build -o /auth-api

EXPOSE 8081

# Run
CMD [ "/auth-api" ]
