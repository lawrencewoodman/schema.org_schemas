# schema.org_schemas

* [schema.org_schemas Github Repository](https://github.com/LawrenceWoodman/schema.org_schemas)

## Description
This repo contains the microdata schemas published on [schema.org](http://schema.org).
It was scraped using v0.2.3 of
 [schema.org_scraper](http://github.com/LawrenceWoodman/schema.org_scraper), to
aid the implementation of software using these schemas and to track the changes
to the types over time.

## Tagging
The repo is tagged with the version of the schemas scraped from
[schema.org](http://schema.org) site.

## Formats
The schemas are in JSON and YAML and below is an explanation of the fields:

### Root(Type) fields

<dl>
  <dt>name</dt>
  <dd>The name of the type. For vocabularies this is the itemtype less the
      prefix of <code>http://schema.org/</code></dd>

  <dt>description</dt>
  <dd>A description of the type</dd>

  <dt>ancestors</dt>
  <dd>The line of ancestors that this type came from</dd>

  <dt>vocabularies</dt>
  <dd>The vocabularies that have their properties included in the type</dd>
  
  <dt>properties</dt>
  <dd>The properties for this type</dd>

  <dt>instances</dt>
  <dd>These are the values that the type can take. For vocabularies, these are
      the canonical references that represent something of this type and should
      be used with the <code>&lt;link&gt;</code> tag along with the
      <code>http://schema.org/</code> prefix</dd>
</dl>

### Properties(Property) Fields

<dl>
  <dt>name</dt>
  <dd>The name of the property</dd>

  <dt>types</dt>
  <dd>The types that the property can take, not forgetting that currently
      Text is assumed as a backup incase one of the specified types isn't
      used.</dd>

  <dt>description</dt>
  <dd>A description of the property</dd>
</dl>
