  # mloda.ai                                                                                                                                                                                                                  
                                                                                                                                                                                                                           
  **Open Data Access for AI and ML**                                                                                                                                                                                       
                                      
  mloda is an open-source data access layer that connects AI tools to data sources reliably. Describe what data you need - mloda delivers it.

  ## Repositories

  | Repository | Description |
  |------------|-------------|
  | [**mloda**](https://github.com/mloda-ai/mloda) | Core Python library. Plugin-based, traceable, framework-agnostic data access for AI agents and ML pipelines. |
  | [**mloda-registry**](https://github.com/mloda-ai/mloda-registry) | Community and enterprise plugins, registry tooling, and development guides. |
  | [**mloda-plugin-template**](https://github.com/mloda-ai/mloda-plugin-template) | Template for creating your own FeatureGroups, ComputeFrameworks, and Extenders. |

  ## Quick Start

  ```bash
  pip install mloda

  from mloda.user import PluginLoader, mloda
  PluginLoader.all()

  result = mloda.run_all(
      features=["customer_id", "income", "income__sum_aggr", "age__avg_aggr"],
      compute_frameworks=["PandasDataFrame"],
      api_data={"SampleData": {
          "customer_id": ["C001", "C002", "C003", "C004", "C005"],
          "age": [25, 35, 45, 30, 50],
          "income": [50000, 75000, 90000, 60000, 85000]
      }}
  )
```

  Why mloda?

  - Declarative - AI agents describe data needs, mloda resolves execution
  - Plugin-based - Compose transformations without orchestration code
  - Traceable - Full lineage from results back to source data
  - Framework-agnostic - Works with Pandas, Polars, Spark, and custom backends
  - Private - Runs on your infrastructure, no data leaves your systems

  Get Involved

  - Browse community plugins in the https://github.com/mloda-ai/mloda-registry
  - Create your own plugin using the https://github.com/mloda-ai/mloda-plugin-template
  - Read the https://mloda.ai
