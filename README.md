# Epipolar Geometry Estimation: Fundamental Matrix, Eight Point Algorithm, and RANSAC

The **Fundamental Matrix** encapsulates the geometric relationship between corresponding points in stereo images, providing essential information for rectification, stereo reconstruction, and 3D scene understanding.

The **Eight-Point Algorithm** is a robust method for estimating the Fundamental Matrix from point correspondences between stereo image pairs.
With the complements of **RANSAC**, Eight Point Algorithm can effectively find the best fundamental matrix estimation to fit relate the stereo data keypoints.

## Results

<table>
    <thead>
        <tr>
            <th></th>
            <th>Left Image</th>
            <th>Right Image</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Original</th>
            <td rowspan=1>
                <img src="./kusvod2/corrA.png", width="400">
            </td>
            <td rowspan=1>
                <img src="./kusvod2/corrB.png", width="400">
            </td>
        </tr>
        <tr>
            <th>Key Points</th>
            <td rowspan=1>
                <img src="./assets/keypoints-A.png", width="400">
            </td>
            <td rowspan=1>
                <img src="./assets/keypoints-B.png", width="400">
            </td>
        </tr>
        <tr>
            <th>Epipolar Line</th>
            <td rowspan=1>
                <img src="./assets/epipolar-A.png", width="400">
            </td>
            <td rowspan=1>
                <img src="./assets/epipolar-B.png", width="400">
            </td>
        </tr>
        <tr>
            <th>RANSAC Epipolar Line</th>
            <td rowspan=1>
                <img src="./assets/epipolar-re-A.png", width="400">
            </td>
            <td rowspan=1>
                <img src="./assets/epipolar-re-B.png", width="400">
            </td>
        </tr>
    </tbody>
</table>

## Usage

The main code is in [eight_point_algorithm.ipynb](./eight_point_algorithm.ipynb)

## Dependencies

The project uses `python==3.12.2`, and the dependencies can be installed by running:

```
pip install -r requirements.txt
```

## References

- [In Defense of the Eight-Point Algorithm](https://ieeexplore.ieee.org/document/601246)
- [Revisiting Hartley's Normalized Eight-Point Algorithm](https://ieeexplore.ieee.org/document/1227992)
- [Intrinsic and Extrinsic Matrices | Camera Calibration](https://youtu.be/2XM2Rb2pfyQ?si=n0okRbjoDhTG-MV-)
- [Overview | Uncalibrated Stereo](https://youtu.be/dUDMQ6dwWDA?si=3gW8P4gI7PN6oJUw)
- [Problem of Uncalibrated Stereo | Uncalibrated Stereo](https://youtu.be/v30I-BqGfuI?si=eb93AsN5UxrGsPsJ)
- [Epipolar Geometry | Uncalibrated Stereo](https://youtu.be/6kpBqfgSPRc?si=Ujg5QJrS5l7C-sw9)
- [Estimating Fundamental Matrix | Uncalibrated Stereo](https://youtu.be/izpYAwJ0Hlw?si=HkibvPryj96pd37o)
- [Finding Correspondences | Uncalibrated Stereo](https://youtu.be/erpiFudDBlg?si=4w5IbkmpIJW84SS0)
