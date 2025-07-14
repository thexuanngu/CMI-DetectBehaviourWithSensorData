# CMI-DetectBehaviourWithSensorData

## Dataset Download Instructions
* Sign up for a free account at [Kaggle](https://www.kaggle.com).
* In your profile, open the **Account** tab and click **Create new API token**.  
  This downloads a file called `kaggle.json` containing your API credentials.
* Move the credentials file to the Kaggle configuration directory and secure its permissions:

```bash
mkdir -p ~/.kaggle
mv ~/Downloads/kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```

With the credentials in place, download and unzip the dataset:

```bash
# Create a virtual environment and install dependencies
cd CMI-DetectBehaviourWithSensorData
python3 -m venv .venv  # or use `python` instead of `python3`
source .venv/bin/activate
pip install -r requirements.txt

# Download and unzip the dataset
kaggle competitions download -c cmi-detect-behavior-with-sensor-data -p data
unzip data/cmi-detect-behavior-with-sensor-data.zip -d data
rm data/cmi-detect-behavior-with-sensor-data.zip
```
