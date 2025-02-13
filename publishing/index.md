<img src="/svg/satellite.svg" align="left" width="100" style="padding-right: 10px;" />

A lot of work remains to do to make publication of content on asteroids easy.

So far, gnAsteroid is not easy enough for non-technical people. Fast deployments using `rsync` are mostly just for VPS or self-hosted servers.

The roadmap is:

1. [x] packaging gnAsteroid. 
2. [ ] work on inter-asteroids links.
3. [ ] **easy publication** for everybody, including:
    * Influencers, 
    * Tinkerers,
    * GNO enthusiasts,
    * Students not in CS,
    * Cosmonauts,
    * techies w/o a lot of time.

### Overview

| Host                | monthly cost  | easiness (technicians) | easiness (non-techie) | rsync     |
| --------------      | ------------- | -------------------   | ------------------------ | --------- |
| [Publish on VPS](vps.md)       | 1-5$          | ★★★★★                 | ★★★☆☆²                   | ✓         |
| [Publish on Vercel](vercel.md) | free          | ★★★★☆                 | ★★☆☆☆                    | ✗³        |
| [Publish on Akash](akash.md)   | 0.5-2$        | ★★☆☆☆                 | ★☆☆☆☆                    | TBD       |

It seems certainly possible to publish on DigitalOcean, AWS or Netlify but no one has done it yet (feel free to [propose an HOWTO](https://github.com/gnAsteroid/gnAsteroid/wiki)). So this list is to expand.


*Footnotes*:

²: with a guide, publishing on something like DigitalOcean may be easy enough for non-techies (TODO).

³: without `rsync` you would have to redeploy your asteroid each time you make an update, therefore Vercel is only suitable for asteroids that don't get updated a lot.


