FROM julia:1.9.3

WORKDIR /app
COPY Project.toml Manifest.toml ./
RUN julia --project -e 'using Pkg; Pkg.instantiate()'
COPY src/ ./src/

EXPOSE 5050

ENTRYPOINT [ "julia", "--project", "src/Main.jl" ]