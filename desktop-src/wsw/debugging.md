---
title: " (Windows Web 服務的調試) "
description: 一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Windows 的 Web 服務偵錯工具
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838678"
---
# <a name="debugging-windows-web-services"></a> (Windows Web 服務的調試) 

一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。


有一些函式和環境變數僅適用于偵錯工具模式。 可以用來協助測試和偵測。

-   設定 WsTimeout = 0 會導致所有的超時都是無限的。 當您在時間緊迫的作業期間逐步執行偵錯工具時，這會很有用。
-   設定 WsFailCount 與呼叫 WsSetAutoFail 的效果相同。
-   WsFlags 可讓您設定各種旗標來修改執行時間行為。 語法為 WsFlags = a、b、c。 支援的旗標為 ModifyTimestamp、ModifyInclusivePrefixes、ModifyTimestampDigest、ModifyToHeaderDigest 和 ModifySignatureValue。

下列函式可用於進行調試：

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




