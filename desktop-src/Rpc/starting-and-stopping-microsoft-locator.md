---
title: 啟動和停止 Microsoft 定位器
description: 必要時，RPC 執行時間程式庫會自動啟動 Microsoft 定位器。 例如，您可以手動停止和啟動定位器，例如，當您在將分散式應用程式進行偵錯工具時，需要清除資料庫時。
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281419bc2a869d43863f946c1fcb172da2f86c04186ba775766233d4caa65c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017548"
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

 

 




