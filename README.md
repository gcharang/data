# README

Edit the file: https://github.com/gcharang/data/info/ecosystem.json and submit a PR

Each time the explorer is opened, a random number is generated in the users browser. It is used to pick a Project, then an ad in it based on their respective priorities and frequencies specified.

All the fields are self explanatory. For projects, `priority` is the number of times with respect to other projects the given project is selected. For ads, `frequency` is similar. The values for `frequency` and `priority` must be integers.

Example:

- two projects have priorities 1 and 1, they will be selected with equal probability
- two projects have priorities 1 and 2, their selection probability is in the ratio `1:2` i.e., if the explorer is opened 100 times, first project is selected 33 times and second project is selected 66 times
- only one project can have `always`, it will be always selected. other projects are ignored
- more than one project can have `never`, theya are always ignored

The same rules apply for ads and their frequencies.

It is recommended to check the validity of the `json` being submitted using websites such as https://codebeautify.org/jsonvalidator

The data part of an ad is seperated into many parts to make it easy to customize.

Example:

```json
{
  "string1": "Version '0.3.6b' is available for Agama.",
  "anchorText": "Click here",
  "link": "https://komodoplatform.com/komodo-wallets/",
  "string2": "to download!"
}
```

Is rendered as
![data-rendered](./example-render.png)

FIN
