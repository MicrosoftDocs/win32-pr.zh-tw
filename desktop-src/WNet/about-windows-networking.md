---
title: 關於 Windows 網路
description: 應用程式可以使用 WNet 函式來新增和取消網路連接，以及取得目前網路設定的相關資訊。
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows 網路 WNet，描述
- WNet WNet，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022054"
---
# <a name="about-windows-networking"></a>關於 Windows 網路

應用程式可以使用 WNet 函式來新增和取消網路連接，以及取得目前網路設定的相關資訊。

下圖顯示一般網路的結構。

![一般網路結構](images/csnet-01.png)

在上圖中，Windows NT Server/Windows 2000 伺服器資源的階層會詳細提供為網路提供者 \# 1。 來自其他提供者的網路資源具有不同的階層式系統。 應用程式開始使用網路之前，不需要階層的相關資訊。 它可以從網路根目錄進行 (也就是最上層的容器資源) ，並在需要資訊時取得網路資源的相關資訊。

包含其他資源的網路資源稱為「 *容器*」（container）。 容器資源是上圖中的方塊。

不包含其他資源的資源稱為 *物件*。 在上圖中，Sharepoint \# 1 和 sharepoint \# 2 是物件。 *Sharepoint* 是可在網路上存取的物件。 Sharepoints 的範例包括印表機和共用目錄。

 

 




