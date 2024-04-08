FROM python:3.12

WORKDIR /src

RUN pip install poetry
RUN poetry config virtualenvs.in-project true
RUN if [ -f ./pyproject.toml ]; then poetry install --no-root; fi
# RUN cd /src && if [ -f ./pyproject.toml ]; then poetry install --no-root; fi
# ENTRYPOINT ["poetry", "run", "uvicorn", "main:app", "--host", "0.0.0.0", "--reload"]
ENTRYPOINT poetry run uvicorn main:app --host 0.0.0.0 --reload