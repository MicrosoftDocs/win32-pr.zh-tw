---
title: 執行緒安全性
description: 此 API 中的所有函數都可以安全地從不同的執行緒呼叫。 不過，以參數形式傳遞給函式的每個物件都有特定的執行緒行為，如下所述。
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- 適用于 Windows 的執行緒安全 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684245"
---
# <a name="thread-safety"></a>執行緒安全性

此 API 中的所有函數都可以安全地從不同的執行緒呼叫。 不過，以參數形式傳遞給函式的每個物件都有特定的執行緒行為，如下所述。


下列控制碼為單一執行緒，且不支援特定實例的並行作業：

-   [WS \_ 堆積](ws-heap.md)
-   [WS \_ 訊息](ws-message.md)
-   [WS \_ XML \_ 緩衝區](ws-xml-buffer.md)
-   [WS \_ XML \_ 讀取器](ws-xml-reader.md)
-   [WS \_ XML \_ 寫入器](ws-xml-writer.md)
-   [WS \_ 錯誤](ws-error.md)
-   [WS \_ 操作 \_ 內容](ws-operation-context.md)
-   [WS \_ 原則](ws-policy.md)
-   [WS \_ 中繼資料](ws-metadata.md)
-   [WS \_ 安全性 \_ 權杖](ws-security-token.md)
-   [WS \_ 安全性 \_ 內容](ws-security-context.md)

下列控制碼是無限制執行緒，可支援特定實例的並行作業：

-   [WS \_ 通道](ws-channel.md)
-   [WS \_ 接聽程式](ws-listener.md)
-   [WS \_ 服務 \_ 主機](ws-service-host.md)
-   [WS \_ 服務 \_ PROXY](ws-service-proxy.md)

針對所有這些控制碼，執行緒是以作業的方式定義， (不) 函式呼叫。 以同步方式叫用的函式與非同步叫用的函式會有不同的定義作業：

-   如果是以同步方式叫用的函式，則作業會在函數執行期間暫止。
-   針對以非同步方式叫用的函式，如果函式傳回 **非 \_ \_ ASYNC** 的傳回碼，則作業會在函數執行期間暫止。 但是，如果函式傳回 **ws \_ S \_ async** ，則作業會暫止，直到 [**叫用 WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) 為止。 如需非同步叫用函數的詳細資訊，請參閱 [非同步模型](asynchronous-model.md) 主題。 如需錯誤碼，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。

若無法追蹤物件的執行緒合約，將會導致未定義的行為。

 

 




