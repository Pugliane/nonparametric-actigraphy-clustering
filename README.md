
---

# Input Data & Environment Setup

---

## Environment Setup

### 1. Create a virtual environment

```bash
python -m venv venv
```

This creates a folder called `venv/` containing an isolated Python environment.

---

### 2. Activate the environment

**Linux / Mac**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

Once activated, your terminal should display `(venv)`.

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

This is where the `requirements.txt` file is used to install all required packages.

---

##  Input Data Format

The script expects a tabular dataset (CSV or Excel), where each row represents one participant.

---

###  Required Columns

```text
Participant, Sex, Age, PLR, Diabetes status, Light Perception
```

---

###  Variables

```text
SRI, SleepMidpoint, RA, IV, IVm, IS, ISm,
M10, M10o, L5, L5o,
ADAT, CoG, FSoD,
kRA, kAR, LRI,
M10olight, L5olight
PeriodActivity, QPActivity,
PeriodLight, QPLight,
PeriodTemperature, QPTemperature
```

---

##  Example Dataset

### Columns

```text
Participant, Sex, Age, PLR, Diabetes status, SRI, SleepMidpoint, RA, IV, IVm, IS, ISm, M10, M10o, L5, L5o, ADAT, CoG, FSoD, kRA, kAR, LRI, M10olight, L5olight, PeriodActivity, QPActivity, PeriodLight, QPLight, PeriodTemperature, QPTemperature, Light Perception
```

---

### Sample Rows

```text
P01F45R0,1,45,1,0,42.58599722029186,1567,0.8516305355296401,0.7459553654401433,0.4143180933784019,0.604094656473627,0.6692002854857269,2999.867780191023,450,240.3766666666667,1490,949.2453870340346,51.13217102941918,0.0936318257449705,0.1935977798185335,0.0227495154509179,69.8828,437,1441,1440,21.640384564431,1440,6.832480203412753,1445,30.1695482745072,1440,1440,1

P02F34R0,1,34,1,0,15.23871527777779,1551,0.8025988707845458,0.6601915396691904,0.451798077181202,0.609662772808506,0.4894042339742607,2678.469168130317,320,293.3169696969697,1460,967.066796817624,47.0231929078461,0.1082034992184743,0.1344632422555327,0.0258771561673868,65.3255,416,1442,1440,9.003007524486954,1440,8.7239032508254,1440,25.26899551484653,1440,1440,1
```

---

##  Important Notes

* Binary variables must be encoded as:

  * `0 = No`
  * `1 = Yes`

* Column names must match exactly those expected by the script.

* Additional variables can be included if needed.

* If you modify the dataset structure, you **must update the settings block in the script accordingly**.

---

##  Customization

You can adapt the pipeline to your dataset by:

* Adding new variables
* Removing unused columns
* Renaming variables

Just make sure to update the corresponding configuration/settings block in the script.


