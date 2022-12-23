# Visual Quality Control with AWS Lookout for Vision

## Project description

Amazon Web Services (AWS) provides a Lookout for Vision service for detecting anomalies in images. This is a convenient AutoML service, but is often requires the development of custom video stream preprocessors to integrate the service for use in real-world scenarios, as well as the preparation of labeled datasets to train the anomaly detection model. In this starting kit, we demonstrate how to build an advanced video preprocessor and integrate it with AWS Lookout for Vision using for industry that are using conveyor belts during the manufacturing process.

## How to Use the starting kit

- Create named profiles under the  `~/.aws/credentials (Linux & Mac) or %USERPROFILE%\.aws\credentials (Windows)`
- Provide name of the lookout project, bucket and location and stored them in config.yml
- If s3 bucket is not created, run cell `Create bucket`
- Store video file that should be processed under the `./data/raw/` folder
- (Optional) Adjust hyperparameters in notebook `aws_video_quality_control_starting_kit` under `Object detection functions`, `Lookout for vision related functions` and `Multi-object tracking` sections
- Run notebook e2e

## Useful Link 

Costs of AWS services used in this notebook

- Data storage - https://aws.amazon.com/s3/pricing/
- Model training - https://aws.amazon.com/lookout-for-vision/pricing/ (Training/Hours)
- Deployed model inference - https://aws.amazon.com/lookout-for-vision/pricing/ (Cloud Inference/Hours)