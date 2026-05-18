# QuestionMarkGalaxy

Unsupervised palette compression on **questionmark1**: **MiniBatchKMeans** (mini-batch k-means, scikit-learn–compatible API) partitions a large set of RGB pixel samples into *k* clusters and exposes each cluster centroid as a discrete swatch, trading high-cardinality colour sets for a low-cardinality representative palette. This repository holds one analysis session—the source frame plus **22** derived stills—using the same layer-exposure workflow as [Exposing-the-Unseen-Layers-of-Paintings](https://github.com/NeuroGamingLab/Exposing-the-Unseen-Layers-of-Paintings).

The repository is organized as **one folder per subject** (`images/`). Each file is a still from a single **questionmark1** session.

**The application** treats each still as a field of color samples. **MiniBatchKMeans**—a lightweight **k-means** variant built for large batches—clusters tens of thousands of extracted colors into a **small set of representative swatches**. That cuts storage and downstream work, makes palettes easier to compare across layers or sessions, and summarizes palette structure without tuning every hue by hand. The approach is vector clustering in color space, chosen for speed when the raw sample count is large. The stills below the original are **AI-generated layer outputs** from that pipeline: each variant applies the same explanation of the source frame to a different palette partition or layer reconstruction.

| Item | Count |
|------|------:|
| Source (`questionmark1-ORIGINAL.tif`) | 1 |
| Derived stills (timestamp-prefixed `*-questionmark1.tif`) | 22 |
| Gallery layout | 2 × 11 |
| README previews (`images/png/`) | PNG exports of each TIFF |

Source stills are **TIFF** in `images/`; **PNG** copies in `images/png/` are used below so GitHub can render the gallery inline.

## Original — `questionmark1`

![questionmark1-ORIGINAL.tif](images/png/questionmark1-ORIGINAL.png)

**questionmark1** (1651×1320, TIFF) is the reference still for this session. Like the artworks in [Exposing-the-Unseen-Layers-of-Paintings](https://github.com/NeuroGamingLab/Exposing-the-Unseen-Layers-of-Paintings), it is read as a dense field of RGB samples, clustered with **MiniBatchKMeans** into representative swatches so palette structure can be compared across layers without hand-tuning every hue. The derived stills in the next section are alternate layer views of the same source, produced by the same unsupervised palette-compression stack.

## Derived stills (2 × 11)

Each tile uses the explanation above: a **MiniBatchKMeans** palette summary of **questionmark1**, exposed as a discrete layer still. Filenames embed a session timestamp prefix; all tiles share the `questionmark1` stem.

<table>
  <tr>
    <td><img src="images/png/177913431498799-questionmark1.png" alt="177913431498799-questionmark1.png" width="400"/><br/><code>177913431498799-questionmark1.tif</code></td>
    <td><img src="images/png/1779134368378218-questionmark1.png" alt="1779134368378218-questionmark1.png" width="400"/><br/><code>1779134368378218-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779134436163894-questionmark1.png" alt="1779134436163894-questionmark1.png" width="400"/><br/><code>1779134436163894-questionmark1.tif</code></td>
    <td><img src="images/png/17791345046476228-questionmark1.png" alt="17791345046476228-questionmark1.png" width="400"/><br/><code>17791345046476228-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779134561209488-questionmark1.png" alt="1779134561209488-questionmark1.png" width="400"/><br/><code>1779134561209488-questionmark1.tif</code></td>
    <td><img src="images/png/1779134616238087-questionmark1.png" alt="1779134616238087-questionmark1.png" width="400"/><br/><code>1779134616238087-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/17791346754368-questionmark1.png" alt="17791346754368-questionmark1.png" width="400"/><br/><code>17791346754368-questionmark1.tif</code></td>
    <td><img src="images/png/17791347356762738-questionmark1.png" alt="17791347356762738-questionmark1.png" width="400"/><br/><code>17791347356762738-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779134804968284-questionmark1.png" alt="1779134804968284-questionmark1.png" width="400"/><br/><code>1779134804968284-questionmark1.tif</code></td>
    <td><img src="images/png/17791348712366478-questionmark1.png" alt="17791348712366478-questionmark1.png" width="400"/><br/><code>17791348712366478-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779134910699144-questionmark1.png" alt="1779134910699144-questionmark1.png" width="400"/><br/><code>1779134910699144-questionmark1.tif</code></td>
    <td><img src="images/png/17791349756645188-questionmark1.png" alt="17791349756645188-questionmark1.png" width="400"/><br/><code>17791349756645188-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779135039330382-questionmark1.png" alt="1779135039330382-questionmark1.png" width="400"/><br/><code>1779135039330382-questionmark1.tif</code></td>
    <td><img src="images/png/1779135078524933-questionmark1.png" alt="1779135078524933-questionmark1.png" width="400"/><br/><code>1779135078524933-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779135142242959-questionmark1.png" alt="1779135142242959-questionmark1.png" width="400"/><br/><code>1779135142242959-questionmark1.tif</code></td>
    <td><img src="images/png/1779135196048564-questionmark1.png" alt="1779135196048564-questionmark1.png" width="400"/><br/><code>1779135196048564-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/17791352467320168-questionmark1.png" alt="17791352467320168-questionmark1.png" width="400"/><br/><code>17791352467320168-questionmark1.tif</code></td>
    <td><img src="images/png/1779135312150741-questionmark1.png" alt="1779135312150741-questionmark1.png" width="400"/><br/><code>1779135312150741-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779135383259706-questionmark1.png" alt="1779135383259706-questionmark1.png" width="400"/><br/><code>1779135383259706-questionmark1.tif</code></td>
    <td><img src="images/png/17791354553464699-questionmark1.png" alt="17791354553464699-questionmark1.png" width="400"/><br/><code>17791354553464699-questionmark1.tif</code></td>
  </tr>
  <tr>
    <td><img src="images/png/1779135521826357-questionmark1.png" alt="1779135521826357-questionmark1.png" width="400"/><br/><code>1779135521826357-questionmark1.tif</code></td>
    <td><img src="images/png/1779136541491795-questionmark1.png" alt="1779136541491795-questionmark1.png" width="400"/><br/><code>1779136541491795-questionmark1.tif</code></td>
  </tr>
</table>

## Related work

- [NeuroGamingLab/Exposing-the-Unseen-Layers-of-Paintings](https://github.com/NeuroGamingLab/Exposing-the-Unseen-Layers-of-Paintings) — multi-artwork collages from the same **MiniBatchKMeans** palette-compression pipeline.
