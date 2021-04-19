---
description: 許多應用程式都取決於媒體事件之間的時間關聯性 (例如，所收到的 DTMF 數位) 用來判斷要求之作業的本質。
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: 媒體事件計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976404"
---
# <a name="media-event-timers"></a>媒體事件計時器

許多應用程式都取決於媒體事件之間的時間關聯性 (例如，所收到的 DTMF 數位) 用來判斷要求之作業的本質。 例如，在語音信箱應用程式中，兩個連續的 DTMF "1" 數位可能表示「備份兩個區段」或「從訊息開頭重新執行」，取決於兩個數字之間經過多少時間。 在用戶端/伺服器環境中，如果在應用程式執行所在的不同處理器上執行 DTMF 偵測，則在區域網路中的延遲會讓媒體事件之間的時間關聯性變得很有可能扭曲，進而導致這些以時間為基礎的差異可能遺失或變成不可靠。

若要解決此問題，您可以將數個 TAPI 訊息加上時間戳記。 因為這是這些事件之間的相對時間，所以事件的「時鐘時間」並不重要，而且牽涉到倒數第二次的時間，這些時間戳記會使用 [**GetTickCount**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函式所傳回的毫秒解析「從 Windows 啟動以來的時間」。 應用程式必須注意這是伺服器 (或電腦上的滴答計數，此服務提供者直接管理硬體正在執行) ，而且不一定是應用程式執行所在的同一部電腦;因此，這些 TAPI 訊息中的時間戳記只能與彼此進行比較，而不能與應用程式執行所在處理器上的 **GetTickCount** 所傳回的值進行比較。

可能有時間戳記的 TAPI 訊息如下： [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)和 [**行 \_ MONITORTONE**](line-monitortone.md)。 滴答計數會插入這些訊息的 *dwParam3* 中。 如果服務提供者不支援時間戳記 (這會由這些訊息中的服務提供者設定 *dwParam3* 指定為 0) ，則 TAPI 本身會將滴答計數插入所有這些訊息的 *dwParam3* 中 (它會稍微扭曲，但在訊息已到達處理序間通訊配置) 的情況下，則小於應用程式的執行方式。

 

 
