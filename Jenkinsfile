pipeline {
    agent any
    stages {
        stage('Create JSON and build artifacts') {
            steps {
                script{
                def jsonData = '''{
                    "paths" : [
                        {
                            "path" : "/api/v1/fs-ui-services-status",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/fs-ui-services-status",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/fs-ui/last-runs/{domain}/{identifier}",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/fs-ui/last-runs/{domain}/{identifier}",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/fs-ui/metadata",
                            "method" : "GET",
                            "Description" : "Default response for GET ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/fs-ui/refresh-metadata",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/fs-ui/refresh-metadata",
                            "Type" : "Internal"  
                        },
                        {
                            "path" : "/api/v1/models-ui/automl-metadata",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/models-ui/automl-metadata",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/models-job-status/{f_gen_id}",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/models-ui/models-job-status/{f_gen_id}",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/models-last-runs/{f_gen_id}",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/models-ui/models-last-runs/{f_gen_id}",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/models-metadata",
                            "method" : "GET",
                            "Description" : "Default response for GET /api/v1/models-ui/models-metadata",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/auto-ml/hyper-para-tune",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/auto-ml/hyper-para-tune",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/form-submit",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/form-submit ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/fs-ui/submit-feature-gen-request",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/fs-ui/submit-feature-gen-request",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/fs-ui/validate-queries",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/fs-ui/validate-queries ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/submit-collection-model-request",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/models-ui/submit-collection-model-request ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/submit-model-request",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/models-ui/submit-model-request",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/update-model-metadata",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/models-ui/update-model-metadata ",
                            "Type" : "Internal"  
                        },
                        {
                            "path" : "/api/v1/models-ui/upload-file",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/models-ui/upload-file",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/models-ui/validate-source",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/models-ui/validate-source ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/service-request",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/service-request ",
                            "Type" : "External"  
                        },
                        {
                            "path" : "/api/v1/validate",
                            "method" : "POST",
                            "Description" : "Default response for POST /api/v1/validate",
                            "Type" : "External"  
                        }
                    ]
                }'''

                writeFile file: 'api-gateway-config.json', text: jsonData

                //Archive the artifacts 
                archiveArtifacts artifacts: 'api-gateway-config.json', fingerprint: true

                }
            }
        }
    }
}