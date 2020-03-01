<template>
  <client-only placeholder="...Loading">
    <div id="openseadragon1" style="width: 800px; height: 600px;"></div>
  </client-only>
</template>
<script src="/openseadragon/openseadragon.min.js"></script>
<script>
if (process.client) {
  require('openseadragon')
}
import OpenSeadragon from 'use-open-seadragon/lib/types/open-seadragon'

const viewer = {
  ...OpenSeadragon,
  preserveViewport: true,
  visibilityRatio: 1,
  minZoomLevel: 1,
  defaultZoomLevel: 1,
  sequenceMode: true,
  tileSources: [
    {
      '@context': 'http://iiif.io/api/image/2/context.json',
      '@id':
        'https://libimages1.princeton.edu/loris/pudl0001%2F4609321%2Fs42%2F00000001.jp2',
      height: 7200,
      width: 5233,
      profile: ['http://iiif.io/api/image/2/level2.json'],
      protocol: 'http://iiif.io/api/image',
      tiles: [
        {
          scaleFactors: [1, 2, 4, 8, 16, 32],
          width: 1024
        }
      ]
    }
  ]
}
export default {
  title: 'OpenSeaDragon'
}
</script>
