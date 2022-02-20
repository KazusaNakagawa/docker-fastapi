FROM public.ecr.aws/lambda/python:3.8

COPY requirements/prod.txt ${LAMBDA_TASK_ROOT}

# Copy function code
COPY src/app.py ${LAMBDA_TASK_ROOT}

RUN python3 -m ensurepip && \
    pip install -r prod.txt

ADD src ${LAMBDA_TASK_ROOT}

CMD [ "app.handler" ]
