FROM python:3.11

WORKDIR /workspace

# Update and install dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    libssl-dev \
    libffi-dev \
    libxml2-dev \
    libxslt1-dev \
    zlib1g-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Upgrade pip and install Python packages
RUN pip install --upgrade pip

RUN pip install \
    google-cloud-bigquery==3.33.0 \
    pyarrow==18.1.0 \
    db-dtypes==1.4.3 \
    pandas==2.2.3 \
    matplotlib==3.10.3 \
    scikit-learn==1.6.1 \
    seaborn==0.13.2 \
    numpy==2.1.2 \
    scipy==1.15.3 \
    statsmodels==0.14.4 \
    xgboost==3.0.2 \
    plotly==6.1.2 \
    tabulate==0.9.0 \
    snowflake-connector-python==3.15.0 \
    duckdb==1.3.0 \
    openpyxl==3.1.5 \ 
    dbt-duckdb==1.9.3

# Set the default command to run when starting the container
CMD ["/bin/bash"]
