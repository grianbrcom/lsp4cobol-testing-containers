from python:3.8.2

COPY requirements.txt .
RUN apt-get update && \
  apt-get install -y firefox-esr && \
  rm -rf /var/lib/apt/lists/* && \
  pip install --no-cache-dir -r requirements.txt && \
  rm requirements.txt && \
  useradd testuser --shell /bin/bash --create-home ;

RUN mkdir /.cache && chmod a+w /.cache ;

USER testuser

