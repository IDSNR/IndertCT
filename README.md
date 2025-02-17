
# API Client Package

This package provides a client to interact with the API of your product.

## Installation

Install the package via pip:

```bash
pip install IndertCT
```

## Usage

### Importing the Package

```python
from IndertCT_python import Client
```

### Client Initialization

```python
client = Client(apikey='your_api_key', password='your_password')
```

## Methods

### `pred_on_crypt(crs)`

Predicts on the given cryptos.

- **URL:** `https://indertct.me/api/getPredCrypt`
- **Arguments:**
  - `crs`: A string or list/tuple of crypto symbols.

### `pred_on_hour_and_crypt(**kwargs)`

Predicts based on hours and cryptos.

- **URL:** `https://indertct.me/api/getPredCrHour`
- **Arguments:**
  - `cryptos`: List/tuple of crypto symbols.
  - `times`: List/tuple of times.

### `pred_on_model_name(models)`

Predicts based on model names.

- **URL:** `https://indertct.me/api/postPredNames`
- **Arguments:**
  - `models`: A string or list/tuple of model names.

### `pred_all_models()`

Gets all model names.

- **URL:** `https://indertct.me/api/modelNames`
- **Arguments:** None

### `start_trading(**kwargs)`

Starts trading.

- **URL:** `https://indertct.me/api/StartTrading`
- **Arguments:**
  - `password`: Password for authentication.
  - `ndays`: Number of days to run trading (integer).
  - `test`: Boolean indicating if this is a test.

### `stop_trading(**kwargs)`

Stops trading.

- **URL:** `https://indertct.me/api/StopTrading`
- **Arguments:**
  - `password`: Password for authentication.

### `get_tickers_binance()`

Gets tickers from Binance.

- **URL:** `https://indertct.me/api/getTickersApi`
- **Arguments:** None

### `manual_trading(**kwargs)`

Performs manual trading.

- **URL:** `https://indertct.me/api/manualTrade`
- **Arguments:**
  - `password`: Password for authentication.
  - `symbol`: Symbol for trading (string).
  - `quantity`: Quantity to trade (int/float).
  - `buy`: Boolean indicating buy or sell.

### `historical_data(**kwargs)`

Gets historical data.

- **URL:** `https://indertct.me/api/historicalCr`
- **Arguments:**
  - `password`: Password for authentication.
  - `times`: Dictionary of time ranges.
  - `limit`: Limit of data points (optional, default is a large number).
  - `crs`: A string or list/tuple of cryptos.
  - `custom data`: Custom data (optional, dictionary).

### `handle_privs(**kwargs)`

Handles privileges for models.

- **URL:** `https://indertct.me/api/handlePrivs`
- **Arguments:**
  - `password`: Password for authentication.
  - `method`: Method to handle privileges (string).
  - `models`: A string or list/tuple of model names.

### `handle_fav_pubs(**kwargs)`

Handles favorite public models.

- **URL:** `https://indertct.me/api/handleFavPubs`
- **Arguments:**
  - `password`: Password for authentication.
  - `method`: Method to handle favorite public models (string).
  - `models`: A string or list/tuple of model names.

### `handle_trading_variables(**kwargs)`

Handles trading variables.

- **URL:** `https://indertct.me/api/handleTradingVariables`
- **Arguments:**
  - `password`: Password for authentication.
  - `data`: List of trading variables (list).