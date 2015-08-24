# Introduction #

The current parser sucks. It treats ASN-1 structures as a big "any" type, and tries its best.

Since it's not possible to correctly parse an X.509 certificate as an "any" type, there are a number of hacks in it handcrafted to parse some X.509 certificates.
Those hacks end up breaking the parsing of other certificates.

So it's a mess, and it's got to go.

# Details #

The new parser is currently being built around the following concepts:
  * use ASN-1 modules to parse and validate ASN-1 data.
  * make it easy to see the ASN-1 structure in the as3 source code (alternatively, if speed becomes an issue, write a generator that outputs as3 code given some ASN-1 structures.)
  * when in doubt, specs shall be read.

That's it for now.

Check in the SVN trunk HEAD for `com/hurlant/util/asn1/*` and `com/hurlant/util/der/Type2.as` to see what's there.