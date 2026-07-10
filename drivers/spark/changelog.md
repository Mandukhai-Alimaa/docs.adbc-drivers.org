---
# Copyright (c) 2026 ADBC Drivers Contributors
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#         http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
{}
---

# Changelog for Apache Spark Driver

## v0.1.0-alpha.3 (2026-07-10)

New features:

- Properly release Spark Connect sessions on disconnect
- Add the `spark.ingest.location` option for bulk ingest staging
- Improve compatibility with Spark Connect on Amazon EMR
- Improve compatibility with Livy on Amazon EMR
- Allow configuring the S3 endpoint used for ingest
- Parse username and password from the connection URI
- Support TLS configuration
- Include the backend name in the reported version
- Add support for Spark 3.5 with Livy
- Implement `GetObjects` for Spark Connect
- Support the `spark://` URI scheme
- Implement column metadata in `GetObjects`
- Report the vendor version via Thrift `GetInfo`
- Add a Spark Connect client implementation

Fixes:

- Accept `auth_type=none` for Livy
- Accept no username with Spark Connect when `auth_type=none`
- Stop hardcoding MinIO test credentials
- Enable the `thrift+http` path
- Properly release memory internally
- Return the correct error code from `SetOption`
- Fix transport wrapper ordering
- Stop requiring an AWS region

Documentation:

- Document additional Livy caveats
- Note Amazon EMR compatibility limitations
- Improve the type table and related docs

## v0.1.0-alpha.2 (2026-06-02)

- Initial release
