---
description: 當您開始事件追蹤會話之後，就可以使用 TraceSetInformation 來指示系統傳回其他事件追蹤資料。
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: 正在抓取其他事件追蹤資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393896"
---
# <a name="retrieving-additional-event-tracing-data"></a>正在抓取其他事件追蹤資料

當您開始事件追蹤會話之後，就可以使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 來指示系統傳回其他事件追蹤資料。 其他資訊將會放在相關事件追蹤的 [擴充資料] 區段中。

下列程式描述如何使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式，從事件追蹤會話取出其他資料。

**取出其他事件追蹤資料**

1.  透過呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)來啟動您的會話。

    如需詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

2.  呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 來設定其他事件追蹤資料。

    使用 *ClassInformation* 參數中的 [**事件 \_ 資訊 \_ 類別**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)列舉來描述您想要取得的其他資訊。 下列範例描述如何使用從 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)呼叫傳回的會話控制碼，以及來自 **事件 \_ 資訊 \_ 類別** 的 **TraceProviderBinaryTracking** 值，來呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)。

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  或者，您可以使用 [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) 來取得目前事件追蹤會話設定的相關資訊。

    如同 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)， [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) 會使用 [**EVENT \_ INFO \_ 類別**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) 列舉來描述要從系統中取出的資訊。

 

 
