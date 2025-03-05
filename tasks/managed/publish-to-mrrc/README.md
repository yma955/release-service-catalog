# publish-to-mrrc

Tekton task that publishes the maven artifacts to MRRC(maven.repository.redhat.com) service. MRRC is used to host maven artifacts of Red Hat Middleware products.
This task will work with [collect-mrrc-task](../collect-mrrc-params/README.md) together to do the MRRC publishment work. It accepts the `mrrc.env` file from the [collect-mrrc-task](../collect-mrrc-params/README.md) and use the variables in it as parameters for the MRRC publishing task.

## Parameters

| Name                 | Description                                                                            | Optional | Default value |
| -------------------- | -------------------------------------------------------------------------------------- | -------- | ------------- |
| caTrustConfigMapName | The name of the ConfigMap to read CA bundle data from                                  | Yes      | trusted-ca    |
| caTrustConfigMapKey  | The name of the key in the ConfigMap that contains the CA bundle data                  | Yes      | ca-bundle.crt |
| mrrcParamFilePath    | Path of the mrrc.env file which contains the MRRC parameters as environment viariables | No       | -             |
| charonAWSSecret      | The secret which contains the aws credential settings for the charon usage             | No       | -             |
| charonSignCASecret   | the secret name for ca files for radas signing                                         | No       | -             |
