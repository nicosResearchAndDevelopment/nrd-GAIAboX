# P.BO.agent.memberOf

## fno

```turtle
@prefix fno: <https://fno.io/spec/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix gbx: <https://www.nicos-rd.com/GAIAboX/> .

gbx:agentMemberOfExecution
    a                    fno:Execution ;
.
```

## Execution request

```http request
POST /data/P/BO/agent/memberOf
Host: https://gbx.nicos-ag.com

{
  "@context" : "https://gbx.nicos-ag.com/data/contexts/context.jsonld",
  "@type" : "gbx:agentMemberOfExecutionParameter",
  "gbx:agentLeftOperand": {
    "fno:type": "foaf:agent",
    "gbx:agent": {
      "@type": "xsd:anyURI",
      "@value": "https://gbx.nicos-ag.com/users/jlangkau" 
    }
  },
  "gbx:agentRightOperand": {
    "fno:type": "foaf:agent",
    "gbx:agent": {
      "@type": "xsd:anyURI",
      "@value": "https://gbx.nicos-ag.com/groups/admin" 
    }
  }
}

```

---