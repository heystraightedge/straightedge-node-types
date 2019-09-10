# straightedge-node-types
This repo contains Typescript bindings for custom straightedge-node modules. In order to use the standard API against Straightedge you must import these types into the Polkadot API as is shown below.

After adding this npm module to your project, use the following snippet to connect an API 
```
import { ApiOptions } from '@polkadot/api/types';
import { ApiRx } from '@polkadot/api';
import { IdentityTypes } from 'straightedge-node-types/dist/identity';
import { VotingTypes } from 'straightedge-node-types/dist/voting';
import { SignalingTypes } from 'straightedge-node-types/dist/signaling';

const options: ApiOptions = {
  provider : new WsProvider('ws://localhost:9944'),
  types : {
    ...IdentityTypes,
    ...SignalingTypes,
    ...VotingTypes,
  },
};

const api = new ApiRx(options);
```
