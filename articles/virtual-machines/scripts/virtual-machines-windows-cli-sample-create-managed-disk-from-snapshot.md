---
title: Create a managed disk from a snapshot - CLI Sample
description: Azure CLI Script Sample - Create a managed disk from a snapshot
services: virtual-machines-windows
documentationcenter: storage
author: ramankumarlive
manager: kavithag

tags: azure-service-management

ms.assetid:
ms.service: virtual-machines-windows
ms.devlang: azurecli
ms.topic: sample
ms.tgt_pltfrm: vm-windows
ms.workload: infrastructure
ms.date: 05/19/2017
ms.author: ramankum
ms.custom: mvc
---

# Create a managed disk from a snapshot with CLI

This script creates a managed disk from a snapshot. Use it to restore a virtual machine from snapshots of OS and data disks. Create OS and data managed disks from respective snapshots and then create a new virtual machine by attaching managed disks. You can also restore data disks of an existing VM by attaching data disks created from snapshots.

[!INCLUDE [sample-cli-install](../../../includes/sample-cli-install.md)]

[!INCLUDE [quickstarts-free-trial-note](../../../includes/quickstarts-free-trial-note.md)]

## Sample script

[!code-azurecli[main](../../../cli_scripts/virtual-machine/create-managed-disks-from-snapshot/create-managed-disks-from-snapshot.sh "Create managed disk from snapshot")]

## Script explanation

This script uses following commands to create a managed disk from a snapshot. Each command in the table links to command specific documentation.

| Command | Notes |
|---|---|
| [az snapshot show](https://docs.microsoft.com/cli/azure/snapshot) | Gets all the properties of a snapshot using the name and resource group properties of the snapshot. Id property is used to create managed disk.  |
| [az disk create](https://docs.microsoft.com/cli/azure/disk) | Creates a managed disk using snapshot Id of a managed snapshot |

## Next steps

For more information on the Azure CLI, see [Azure CLI documentation](https://docs.microsoft.com/cli/azure).

Additional virtual machine and managed disks CLI script samples can be found in the [Azure Windows VM documentation](../windows/cli-samples.md?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).
