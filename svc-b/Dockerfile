FROM 580550010989.dkr.ecr.us-west-1.amazonaws.com/bkln4266/s8-builder/debian:12.5-slim AS build
RUN echo built > /artifact.txt

FROM 580550010989.dkr.ecr.us-west-1.amazonaws.com/bkln4266/s8/debian:12.15-slim
COPY --from=build /artifact.txt /artifact.txt

COPY app.sh /app.sh
RUN chmod +x /app.sh

CMD ["/app.sh"]
