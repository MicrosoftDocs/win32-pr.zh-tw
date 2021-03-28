---
title: 設備磁碟機資訊
description: 設備磁碟機和模組很類似，因為它們都是以 PE 檔案為基礎。
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021072"
---
# <a name="device-driver-information"></a>設備磁碟機資訊

設備磁碟機和模組很類似，因為它們都是以 PE 檔案為基礎。 不過，雖然每個進程都有自己的已載入模組私用清單，但是設備磁碟機具有系統的全域模組。 因此，PSAPI.DLL 具有特定的函式，可取得設備磁碟機及其名稱的清單。

您可以藉由呼叫 [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) 函式，來取得每個設備磁碟機的載入位址。 此函式會使用系統中所有設備磁碟機的載入位址，填滿 **LPVOID** 值的陣列。

[**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea)函式會採用驅動程式載入位址做為輸入，並使用驅動程式的基底名稱填入緩衝區 (例如 Win32k.sys) 。 相關的函式 [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea)會採用相同的參數，並傳回設備磁碟機的路徑 (例如，C： \\ Windows \\ System32 \\Win32k.sys) 。

 

 




