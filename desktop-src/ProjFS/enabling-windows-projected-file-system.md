---
title: 啟用 Windows 投射的檔案系統
description: 描述如何在 Windows 上啟用 ProjFS
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/23/2019
ms.locfileid: "106967182"
---
# <a name="enabling-windows-projected-file-system"></a>啟用 Windows 投射的檔案系統

ProjFS 隨附于 Windows 作為選擇性元件。  在提供者可以使用它之前，必須先啟用它。  您可以透過網際網路使用 <!--the GUI or--> 啟用 ProjFS 的 PowerShell。

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>如何使用 PowerShell 啟用 ProjFS

若要使用 PowerShell 來啟用 ProjFS，請 `Enable-WindowsOptionalFeature` 在提高許可權的 PowerShell 視窗中使用 Cmdlet：

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

如果 Enable-WindowsOptionalFeature 報表，請重新開機電腦 `RestartNeeded: True` 。
