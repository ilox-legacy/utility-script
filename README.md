> **Current Version**: 1.2.1

**Please use https://github.com/ilox/utility-script/issues for bug reports and suggestions!**

***

Website: https://ilox.rocks  
Discord: https://discord.gg/NDv2HdmTAD

***

## What is this?

The _ilox utility script_ provides a faster way for adding products. It does __not__ buy you anything or tries to bypass any shop security concepts (like 
captchas, auto form filling, ...). On success the script will show a proper success message and play a sound.

## Disclaimer

I __highly discourage__ you from running __any__ script you find on the internet in your browser. ***Use at your own risk!***

## Usage

*In order to configure the script (e.g. changing the product or using custom IDs) please see below!*

- Head over to one of the supported shops (see below for list of supported shops) in your browser
- Press F12 in your browser and head over to "Console"
- Enter the following code:

```javascript
eval(atob('ZmV0Y2goJ2h0dHBzOi8vdG9vbHMubmVoYWxpc3QuaW8vaWxveC5taW4uanMnKS50aGVuKHIgPT4gci50ZXh0KCkpLnRoZW4ociA9PiBldmFsKHIpKTs='));
```

- Press enter
- Done.

### Example 1: changing the product

In order to set a different product (in this example on MediaMarkt.de):

- Head over to one of the supported shops (see below for list of supported shops) in your browser
- Press F12 in your browser and head over to "Console"
- Enter the following code:

```javascript
window.ILOX_PRODUCT="RTX3060";
```

- Press enter
- Enter the script:

```javascript
eval(atob('ZmV0Y2goJ2h0dHBzOi8vdG9vbHMubmVoYWxpc3QuaW8vaWxveC5taW4uanMnKS50aGVuKHIgPT4gci50ZXh0KCkpLnRoZW4ociA9PiBldmFsKHIpKTs='));
```

- Press enter
- Done.

This will try to add RTX 3060 product IDs to your cart.

### Example 2: setting custom IDs

In order to use custom IDs:

- Head over to one of the supported shops (see below for list of supported shops) in your browser
- Press F12 in your browser and head over to "Console"
- Enter the following code:

```javascript
window.ILOX_PRODUCT="CUSTOM";
window.ILOX_CUSTOM_IDS=[1111, 2222, 3333, 4444];
```

- Press enter
- Enter the script:

```javascript
eval(atob('ZmV0Y2goJ2h0dHBzOi8vdG9vbHMubmVoYWxpc3QuaW8vaWxveC5taW4uanMnKS50aGVuKHIgPT4gci50ZXh0KCkpLnRoZW4ociA9PiBldmFsKHIpKTs='));
```

- Press enter
- Done.

This will now try add the product IDs 1111, 2222, 3333 and 4444 to your cart.

### Example 3: changing configuration

While not being recommended you can for example disable pre- or post validation (see FAQ for further information):

- Head over to one of the supported shops (see below for list of supported shops) in your browser
- Press F12 in your browser and head over to "Console"
- Enter the following code:

```javascript
window.ILOX_POSTVALIDATION=false;
```

- Press enter
- Enter the script:

```javascript
eval(atob('ZmV0Y2goJ2h0dHBzOi8vdG9vbHMubmVoYWxpc3QuaW8vaWxveC5taW4uanMnKS50aGVuKHIgPT4gci50ZXh0KCkpLnRoZW4ociA9PiBldmFsKHIpKTs='));
```

- Press enter
- Done.

### Example 4: test mode

Most shops do offer a `TEST` product to test for success.

- Head over to one of the supported shops (see below for list of supported shops) in your browser
- Press F12 in your browser and head over to "Console"
- Enter the following code:

```javascript
window.ILOX_PRODUCT="TEST";
```

- Press enter
- Enter the script:

```javascript
eval(atob('ZmV0Y2goJ2h0dHBzOi8vdG9vbHMubmVoYWxpc3QuaW8vaWxveC5taW4uanMnKS50aGVuKHIgPT4gci50ZXh0KCkpLnRoZW4ociA9PiBldmFsKHIpKTs='));
```

- Press enter
- Done.

## Supported shops

| Shop | Supported products / Description | Default product |
|------|--------------------|---------|
| MediaMarkt.at | `PS5` | `PS5` |
| MediaMarkt.de | `PS5`, `RTX3060`, `RTX3060TI`, `RTX3070`, `RTX3080`, `RTX3090` | `PS5` | 
| Saturn.de | `PS5`, `RTX3060`, `RTX3060TI`, `RTX3070`, `RTX3080`, `RTX3090` | `PS5` |
| MyToys.de | `PS5` | `PS5` |
| Notebooksbilliger.de | `RTX3000` | `RTX3000`
| Euronics.de | `PS5` | `PS5` |
| Expert.de | `PS5` | `PS5` |
| AMD.com | Enables the "Add to cart" buttons (Idea by PartAlert.net) | - |

Additionally all shops do support a `TEST` product in order to test the script (which uses a usually available product) and a `CUSTOM` product
for using custom product IDs.

## Configuration

The script can be configured before running it with global window variables.

If for some reason you've messed up and ran the script BEFORE you've set the parameters you need to reload the page and start fresh from the beginning.

Configuration parameters:

- `ILOX_PREVALIDATION` (bool): I __highly__ recommend not to set this to `false` since this is responsible for not triggering bot protection (defaut: `true)`
- `ILOX_POSTVALIDATION` (bool): Responsible for telling you if the script worked (default: `true`)
- `ILOX_MMAT_PS5_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_PS5_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_RTX3060_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_RTX3060TI_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_RTX3070_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_RTX3080_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MMDE_RTX3090_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_PS5_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_RTX3060_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_RTX3060TI_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_RTX3070_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_RTX3080_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_SATURN_RTX3080_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_EXPERT_PS5_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_MT_PS5_IDS` (number[]): Default product IDs - better not change that except you know what you're doing
- `ILOX_NBB_RTX3000FE_IDS` (number[]): Default product IDs - better not change that except you know what you're doing

## F.A.Q.

**The script errored. Why?**  
The script is written in a way that it tells you pretty exactly what went wrong. If APIs do not allow for adding products the script is most likely going to fail. Please just 
_read_ what's written in your console to find out what happened.

**What are `PRE`- and `POSTVALIDATION`?**  
The script tries not to run into bot protection and kinda tries to find out if it's going to work (pre-validation) and/or if it has worked (post-validation). Pre-validation 
uses just the API to check if product IDs can be purchased through the API. Post-validation is basically just checking if there's something in your cart.

**I still ran into bot protection. Why?**  
Mostly likely because you've entered the script too many times. Don't do that.
