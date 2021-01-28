# wit.ai integration

Integrates StackStorm with Wit.ai

## Pre-requisites

Please ensure that you have installed:

* libsox and development libraries
* libcurl and development libraries

## Configuration

wit.ai can be configured with any number of applications. As such, when querying
the API, actions can take the `application` parameter, which will send the
request mapped with API keys in the configuration below.

Copy the example configuration in [witai.yaml.example](./witai.yaml.example)
to `/opt/stackstorm/configs/witai.yaml` and edit as required.

* `applications` - Takes a dictionary of application names and access tokens as
                   values.
* `default_application` - Name of the default application to send query if none
                          is specified (Optional)

### Example Configuration

```yaml
---
applications:
  steve: XXXXXX
  sammy: XXXXXX
default_application: steve
```

## Actions

* `text_query` - Send a text based query to wit.ai
