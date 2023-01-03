# `prost_twirp` Release History

## 0.2.0

Released 2023-01-03

* Updated dependencies: prost 0.11, Hyper 1.4, etc.

* Client code will need to be updated as a consequence of the 
  large changes to the Hyper API.
  
* Fixed the generated URL format to match that specified by Twirp,
  e.g. `/twirp/twirp.example.haberdasher.Haberdasher/MakeHat`.
  This breaks network compatibility between any (now very old)
  `prost-twirp` clients and servers, but should restore compatibility
  with other Twirp implementations.
  
* Changed the primary repo to
  <https://github.com/sourcefrog/prost-twirp>.
  
* Removed `PTReq<T>` type alias: just say `ServiceRequest<T>`.

* Dropped the option to embed some library code in the generated code: it makes
  no difference to the binary size or build times, and makes the user model
  more complicated.
  
## 0.1.0

* Initial release.
