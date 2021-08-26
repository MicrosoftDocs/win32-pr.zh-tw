---
description: Mergemod.dll 提供的 COM 物件會針對合併模組執行合併作業和來源映射產生。 主要物件會針對 C/c + + 程式和自動化用戶端（包括 Visual Basic 和 VBScript）來實作為介面。
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: 合併模組自動化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e592429b77671e154b932f3d79f6f57bb39a65ee2058aafd2164428234458acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043048"
---
# <a name="merge-module-automation"></a>合併模組自動化

Mergemod.dll 提供的 COM 物件會針對合併模組執行合併作業和來源映射產生。 主要物件會針對 C/c + + 程式和自動化用戶端（包括 Visual Basic 和 VBScript）來實作為介面。

安裝 Mergemod.dll 的慣用方法是使用 Windows Installer。 包含 Mergemod.dll COM 介面之元件的元件識別碼為 {FD153241-37EC-11D2-8892-00A0C981B015}。 您可以在所有 Windows 系統上使用相同的二進位檔，而 dll 將在舊版系統上透過 regsvr32 自行註冊。

請注意，Mergemod.dll 需要在系統上安裝 Msvcrt.dll。

請注意，需要 Mergemod.dll 2.0 才能建立 [可設定的合併模組](configurable-merge-modules.md)。 Mergemod.dll 版本2.0 會透過 [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) 介面在組建階段提供延伸的功能。 此 CLSID 支援 Mergemod.dll 版本1.0 所提供之 [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) 介面的所有現有功能。 Mergemod.dll 2.0 之 [**Merge**](merge-object.md) 物件的預設介面是 **IMsmMerge2** 介面，而不是 **IMsmMerge** 介面。

[Mergemod.dll 版本1.0 的物件模型](object-model-for-mergemod-dll-version-1-0.md)

[Mergemod.dll 版本2.0 的物件模型](object-model-for-mergemod-dll-version-2-0.md)

 

 
