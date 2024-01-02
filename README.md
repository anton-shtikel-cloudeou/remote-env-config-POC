# remote-env-config-POC 

Here is an example of remote repository specification

Accorring to such repository, your `bdd.config` should have such credentials 

```json
{
  "projectName": "remote-env-config-POC",
  "remoteEnvConfig": {
    "repository": "anton-shtikel-cloudeou",
    "repositoryToken": "your_token"
  }
}
```

Example of importing remote configs from POC repository
```typescript
import { remoteEnv } from "@cloudeou/telus-bdd";


    const stRemoteConfigTS = await remoteEnv().getRemoteEnvConfig<EC>('st', true);
    const devRemoteConfigTS = await remoteEnv().getRemoteEnvConfig<EC>('dev', true);
    const prodRemoteConfigTS =  await remoteEnv().getRemoteEnvConfig<EC>('prod', true)

    const testRemoteConfigJS =  await remoteEnv().getRemoteEnvConfig<EC>('test', false)
```

`Note: projectName must match with name of local project and name of Remote Repository `
