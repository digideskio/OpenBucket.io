# OpenBucket.io

A simple API to store & retrieve JSON objects.

Get your API-Key at http://OpenBucket.io

### Create File
--

**POST** Create a new JSON file

```
curl -X POST -H "Content-Type: application/json" http://api.openbucket.io/new -d '{"key":"YOUR_API_KEY", "content":{"some-key":"Some Value"}}'

```
which returns 

```
{
  "file":"FILE_NAME", 
  "pass":"FILE_PASS"
}
```

**IMPORTANT:** Write down your FILE_NAME and FILE_PASS. This is the only time you get them! You need the FILE_NAME to fetch and FILE_PASS to update your JSON file.

###Fetch Files
--
**GET** Retrieve your public JSON file

```
curl http://api.openbucket.io/FILE_NAME.json
```
###Update Files
--
**POST** Update your JSON file

```
curl -X POST -H "Content-Type: application/json" http://api.openbucket.io/FILE_NAME.json -d '{"pass":"FILE_PASS", "content":{"other-key":"Other Value"}}'

```

<hR>
Some important stuff:
* If you lose your File Name or Pass there's no way to get them back again.
* It's not safe to save Passwords and/or Sensitive information on openbucket.
* Your JSON Object can't be larger than 100kb.
* Play nice (:

