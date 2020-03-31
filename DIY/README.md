# Do it yourself

#### Download it

From [here](../resources/GAIAboX.pdf).

#### Print it

The result will be a paper-version of your own GAIAboX. Cut it out the
 way you think it will be a box-like-thingy at the end.

#### Fold it

...in a way you think it results in a box-like-thingy at the end.

#### Stick it

...together at those regions and in a - - - we think you know it, or?

#### Photograph it

Your work has to be saved for others!

#### Send it

...to GAIAboX@nicos-ag.com and it will be published [here](https://gaiabox.eu/blog/).

#### Control it

If you won't control the usage of your GAIAboX-pic - so, do nothing and
 the picture will *NOT* be shown and your name will *NOT* be published,
 too.

So, if you like to control the usage of your given GAIAbox-pic and/or
 your name, please write some kind of `usage control` in the body of
 same mail the picture is attached to. The `action` performed in
 GAIAboX's-Blog will be `use`. Let's say, we will *publish* the
 information...

##### Short version of "Control it" 

Let us know, if we're allowed to publish your picture
 and your name as author/producer of it.

#### How to control it

- replace `example.org` with your domain
- replace the target `GAIAboX.jpeg` by given GAIAboX-pic file-name
- regarding the picture itself:
 ```json
 {  
    "@context": "http://www.w3id.org/ids/contract.jsonld",  
    "@type": "ids:ContractAgreement",  
    "uid": "http://example.org/policy#use-my-GAIAboX-pic",  
    "permission": {
        "target": "GAIAboX.jpeg",
        "action": "use"
    }
}
 ```
...so put this in your mail and modify it.

If you will send more then one picture please use a list of strings
```text
"target": [ "GAIAboX_1.jpeg", "GAIAboX_2.jpeg", "GAIAboX_3.jpeg" ]
```

- regarding the fact, that you as an author has to be mentioned
  - replace `example.org` with your domain
  - replace `ThisIsMyName` with the name that will be published (maybe a nic-name, too?)
```json
{  
    "@context": "http://www.w3id.org/ids/contract.jsonld",  
    "@type": "ids:ContractAgreement",  
    "uid": "http://example.org/policy#use-my-name",  
    "permission": {
        "target": "ThisIsMyName",
        "action": "use"
    }
}
```
...so put those contracts (policies) into your mail and modify them.

#### Understand it

If you like to understand what `usage control` is, please have
 a look at
 
- [IDS Reference Architecture Model, PDF, page 87](https://www.internationaldataspaces.org/wp-content/uploads/2019/03/IDS-Reference-Architecture-Model-3.0.pdf)

or

- [Specifications hosted in *International Data Spaces* `IDS-G`](https://github.com/International-Data-Spaces-Association/IDS-G/blob/master/core/UsageControl/README.md) .

---
