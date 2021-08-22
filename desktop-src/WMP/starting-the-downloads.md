---
title: 開始下載
description: 開始下載
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，開始下載
- 線上商店，開始下載
- 輸入2個線上商店，開始下載
- Windows Media Player，下載管理員
- Windows Media Player下載管理員
- 下載管理員
- 開始下載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995068"
---
# <a name="starting-the-downloads"></a>開始下載

當使用者按一下 [ **下載**] 時，就會開始下載。 此按鈕在程式碼中名為 btnDownload，而 **onClick** 事件的事件處理常式函式會命名為 "OnDownload"。

"OnDownload" 會先建立新的空白 **DownloadCollection** 物件，並將它指派給本機變數。


```C++
oDLC = g_oManager.createDownloadCollection();

```



接下來，此函式會啟動每五個專案的下載，並將傳回的 **DownloadItem** 物件儲存在陣列中。


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



然後，程式碼會使用下載集合及其下載專案的相關資訊來更新使用者介面元素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用下載管理員**](using-the-download-manager.md)
</dt> </dl>

 

 




