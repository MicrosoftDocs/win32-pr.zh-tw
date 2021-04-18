---
title: " (Windows Web 服務) 的調試"
description: 一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Windows 的 Web 服務偵錯工具
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965879"
---
# <a name="debugging-windows-web-services"></a> (Windows Web 服務) 的調試

一組函式僅適用于 DEBUG 組建，且適用于測試和偵錯工具。


有一些函式和環境變數僅適用于偵錯工具模式。 可以用來協助測試和偵測。

-   設定 WsTimeout = 0 會導致所有的超時都是無限的。 當您在時間緊迫的作業期間逐步執行偵錯工具時，這會很有用。
-   設定 WsFailCount 與呼叫 WsSetAutoFail 的效果相同。
-   WsFlags 可讓您設定各種旗標來修改執行時間行為。 語法為 WsFlags = a、b、c。 支援的旗標為 ModifyTimestamp、ModifyInclusivePrefixes、ModifyTimestampDigest、ModifyToHeaderDigest 和 ModifySignatureValue。

下列函式可用於進行調試：

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




