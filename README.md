# gatekeeper
Simple, quick monitoring tool and bandwidth allocator for Linux

Overview

A terminal-based interactive tool for managing network bandwidth of processes in real-time. Easily throttle, boost, or remove limits from network-active processes with a simple interface.
Features

    🕹️ Interactive dialog-based UI

    🔄 Auto-refreshing process list (every 2 seconds)

    ⏬ Throttle processes to specific bandwidth limits

    ⏫ Boost processes to maximum bandwidth

    🗑️ Remove all bandwidth limits

    📊 Clear visual indicators of process status

    ❓ Built-in help system

Installation
Dependencies
bash
Copy

sudo apt install trickle dialog

Download
bash
Copy

curl -o throttle_manager.sh https://raw.githubusercontent.com/yourrepo/network-throttle-manager/main/throttle_manager.sh
chmod +x throttle_manager.sh

Usage
bash
Copy

./throttle_manager.sh

Interface Guide

    Navigation: Use arrow keys (↑↓) to move between options

    Selection: Press Enter to confirm selection

    Help: Press F1 or select HELP for controls reference

    Exit: Select EXIT or press Esc to quit

Status Indicators
Status	Description
BOOSTED	Process running at maximum speed
THROTTLED	Process limited to specified KB/s
UNMANAGED	No bandwidth limits applied
Examples

    Throttle a process to 100KB/s:

        Select the process from the list

        Choose "THROTTLE"

        Enter "100" when prompted

    Boost a process to maximum speed:

        Select the process from the list

        Choose "BOOST"

    Remove all limits:

        Select the process from the list

        Choose "REMOVE"

Technical Details

    Uses trickle for bandwidth shaping

    Stores throttle settings in /tmp/throttle.log

    Auto-refreshes every 2 seconds (configurable)

Troubleshooting

Error: "trickle not found"
bash
Copy

sudo apt install trickle

Error: "dialog not found"
bash
Copy

sudo apt install dialog

Process not appearing in list?

    Ensure the process has active network connections

    Try refreshing (F5) or waiting for the auto-refresh

DECLASSIFIED BY AGENT CALLSIGN: RIOTMAN
Authorization# : 565552728
Department Of The Unseen, Engineering Division
Declassified for public use under License:

MIT License - Free for personal and commercial use
