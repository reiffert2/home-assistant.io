---
title: Nord Pool
description: Instructions on how to integrate with the Nord Pool Energy market prices.
ha_category:
  - Energy
  - Finance
  - Sensor
ha_release: 2024.12
ha_iot_class: Cloud Polling
ha_config_flow: true
ha_codeowners:
  - '@gjohansson-ST'
ha_domain: nordpool
ha_platforms:
  - sensor
ha_integration_type: integration
---

Integrates [Nord Pool Group](https://www.nordpoolgroup.com/) energy prices into Home Assistant.

{% include integrations/config_flow.md %}

{% tip %}
Only a single configuration entry is supported so ensure you select all the areas of interest when you setup the integration.

EUR is the base currency for market prices, You will find in the `Exchange rate` sensor the relevant conversion used if you choose another currency.
{% endtip %}

## Sensors

### Main sensors

- Current price for the selected area
- Previous price for the selected area
- Next price for the selected area

These sensors can be used to calculate your current cost of energy, should I charge my battery now or next hour etc.

### Block price sensors

- Block average
- Block minimum
- Block maximum
- Block start time
- Block end time

These sensors show the minimum/maximum and average during certain blocks of the day. More known as off-peak (cheaper) or peak hours (expensive).
These sensors are not enabled by default and needs to be enabled to be used.

### Daily average

- Daily average

This sensor is not enabled by default.

### Diagnostic sensors

- Last updated - indicated when the market price was last updated.
- Currency - The selected currency.
- Exchange rate - EUR is the base currency so will show the exchange rate used on the market place.
