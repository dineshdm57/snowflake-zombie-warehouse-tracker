# Snowflake Zombie Warehouse Tracker using OpenOps

Detect Snowflake warehouses running 24/7 but with <5% query load.

## What it Does
- Connects to Snowflake.
- Fetches list of active warehouses and their usage.
- Detects warehouses with very low query load.
- Sends Slack alerts if any warehouse is identified as underutilized.

## How to Use
1. Import the `.json` workflow into OpenOps.
2. Set up your Snowflake connection.
3. Set up your Slack connection.
4. Adjust parameters (time range, load thresholds) if needed.
5. Activate and schedule the workflow to run daily or weekly.

## Requirements
- Snowflake account with access to `WAREHOUSE_LOAD_HISTORY`.
- Slack webhook or connection for sending alerts.

## Customization
- You can easily adapt this to email alerts or dashboards.
- Thresholds (e.g., 5% load) are editable.
- Works for any scale of Snowflake environments.

## Notes
- Only active, running warehouses are evaluated.
- Workflow cleanly ends if no idle warehouses are found.
