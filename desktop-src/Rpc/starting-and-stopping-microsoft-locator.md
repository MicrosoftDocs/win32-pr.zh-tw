---
title: 啟動和停止 Microsoft 定位器
description: 必要時，RPC 執行時間程式庫會自動啟動 Microsoft 定位器。 例如，您可以手動停止和啟動定位器，例如，當您在將分散式應用程式進行偵錯工具時，需要清除資料庫時。
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020733"
---
# <a name="starting-and-stopping-microsoft-locator"></a>啟動和停止 Microsoft 定位器

必要時，RPC 執行時間程式庫會自動啟動 Microsoft 定位器。 例如，您可以手動停止和啟動定位器，例如，當您在將分散式應用程式進行偵錯工具時，需要清除資料庫時。

**若要停止並啟動 Microsoft 定位器**

1.  在主控台中，按一下 [服務] 圖示。

    [ **服務** ] 對話方塊隨即出現。

2.  在 [ **服務** ] 對話方塊中，選取 [ **Microsoft 定位器** ]，然後按一下 [ **啟動** ] 或 [ **停止**]。

您也可以從命令列啟動和停止 Microsoft 定位器，方法是輸入：

**net \[ start/stop \] rpclocator**

只有系統管理員可以在停止後啟動 Microsoft 定位器。 如果已停止，則會視 RPC 執行時間程式庫的需要重新開機。

 

 




