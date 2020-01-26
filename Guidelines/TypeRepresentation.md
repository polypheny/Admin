# Internal Type Representation

This file describes the internal representation of various types in the Enumberable Convention.

**IMPORTANT**: This is a Work In Progress document and may be incomplete and/or inaccurate.

## Representation

| SqlTypeName | Internal Type | Remark |
| ----------- | ------------- | ------ |
| `BOOLEAN` | Boolean | |
| `INTEGER` | Integer | |
| `FLOAT` | Float | |
| `DOUBLE` | Double | |
| `DATE` | int | Days since January 1, 1970, 00:00:00 GMT. Calculate just as timestamp, then integer divide by 86400000 |
| `TIME` | int | Milliseconds since start of day. Calculate just as timestamnp, then modulo 86400000 |
| `TIME_WITH_LOCAL_TIME_ZONE` | int | FILL IN! |
| `TIMESTAMP` | long | Milliseconds since January 1, 1970, 00:00:00 GMT |
| `TIMESTAMP_WITH_LOCAL_TIME_ZONE` | long | FILL IN! |
| `VARCHAR` | String | Not sure? |

## Unknown representation

| SqlTypeName | Internal Type | Remark |
| ----------- | ------------- | ------ |
| `TINYINT` | ? | |
| `SMALLINT` | ? | |
| `BIGINT` | ? | |
| `DECIMAL` | ? | |
| `REAL` | ? | |
| `INTERVAL_YEAR` | ? | |
| `INTERVAL_YEAR_MONTH` | ? | |
| `INTERVAL_MONTH` | ? | |
| `INTERVAL_DAY` | ? | |
| `INTERVAL_DAY_HOUR` | ? | |
| `INTERVAL_DAY_MINUTE` | ? | |
| `INTERVAL_DAY_SECOND` | ? | |
| `INTERVAL_HOUR` | ? | |
| `INTERVAL_HOUR_MINUTE` | ? | |
| `INTERVAL_HOUR_SECOND` | ? | |
| `INTERVAL_MINUTE` | ? | |
| `INTERVAL_MINUTE_SECOND` | ? | |
| `INTERVAL_SECOND` | ? | |
| `CHAR` | ? | |
| `BINARY` | ? | |
| `VARBINARY` | ? | |
| `NULL` | ? | |
| `ANY` | ? | |
| `SYMBOL` | ? | |
| `MULTISET` | ? | |
| `ARRAY` | ? | |
| `MAP` | ? | |
| `DISTINCT` | ? | |
| `STRUCTURED` | ? | |
| `ROW` | ? | |
| `OTHER` | ? | |
| `CURSOR` | ? | |
| `COLUMN_LIST` | ? | |
| `DYNAMIC_STAR` | ? | |
| `GEOMETRY` | ? | |

