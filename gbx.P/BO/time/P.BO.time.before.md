# P.BO.time.before

## fno

```turtle
@prefix fno: <https://fno.io/spec/> .
@prefix time: <http://www.w3.org/2006/time#> .
@prefix gbx: <https://www.nicos-rd.com/GAIAboX/> .

gbx:timeBeforeExecution
    a                    fno:Execution ;
    # TODO: is this the right way to express the parameters?
    #
    # time ontology, 'i'
    gbx:timeLeftOperand  [ fno:type          time:Instant ;
                           time:hasBeginning "2020-06-22T00:00:42.42Z"^^xsd:dateTimeStamp ; ] ;

    #
    fno:executes gbx:timeBeforeFunction ;
    #

    # time ontology 'j'
    gbx:timeRightOperand [ fno:type          time:ProperInterval ;
                           time:hasBeginning "2020-06-24T15:00:00.0Z"^^xsd:dateTimeStamp ;
                           time:hasEnd       "2020-06-28T15:00:42.0Z"^^xsd:dateTimeStamp ; ] ;
.
```

## Execution request

```http request
POST /data/P/BO/time/before
Host: https://gbx.nicos-ag.com

{
  "@context" : "https://gbx.nicos-ag.com/data/contexts/context.jsonld",
  "@type" : "gbx:timeExecutionParameter",
  "gbx:timeLeftOperand": {
    "fno:type"; "time:Instant",
    "time:hasBeginning": {
      "@type": "xsd:dateTimeStamp",
      "@value": "2020-06-24T15:35:19.42Z" 
    }
  },
  "gbx:timeRightOperand": {
    "fno:type"; "time:ProperInterval",
    "time:hasBeginning": {
      "@type": "xsd:dateTimeStamp",
      "@value": "2020-06-24T00:00:00.0Z" 
    },
    "time:hasEnd": {
      "@type": "xsd:dateTimeStamp",
      "@value": "2020-06-25T00:00:0.0Z" 
    }
  }
}

```

same as:

```http request
POST /data/P/BO/time/before
Host: https://gbx.nicos-ag.com

{
  "@context" : "https://gbx.nicos-ag.com/data/contexts/context.jsonld",
  "@type" : "gbx:timeExecutionParameter",
  "gbx:timeLeftOperand": {
    "fno:type"; "time:Instant",
    "time:hasBeginning": {
      "@type": "xsd:dateTimeStamp",
      "@value": "2020-06-24T15:35:19.42Z" 
    }
  },
  "gbx:timeRightOperand": {
    "fno:type"; "time:ProperInterval",
    "time:hasBeginning": {
      "@type": "xsd:dateTimeStamp",
      "@value": "2020-06-24T00:00:00.0Z" 
    },
    "time:duration": {
      "@type": "xsd:duration",
      "@value": "P1D" 
    }
  }
}

```

---