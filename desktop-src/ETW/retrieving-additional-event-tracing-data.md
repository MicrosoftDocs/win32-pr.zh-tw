---
description: 當您開始事件追蹤會話之後，就可以使用 TraceSetInformation 來指示系統傳回其他事件追蹤資料。
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: 正在抓取其他事件追蹤資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943617"
---
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="528be-103">正在抓取其他事件追蹤資料</span><span class="sxs-lookup"><span data-stu-id="528be-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="528be-104">當您開始事件追蹤會話之後，就可以使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 來指示系統傳回其他事件追蹤資料。</span><span class="sxs-lookup"><span data-stu-id="528be-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="528be-105">其他資訊將會放在相關事件追蹤的 [擴充資料] 區段中。</span><span class="sxs-lookup"><span data-stu-id="528be-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="528be-106">下列程式描述如何使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式，從事件追蹤會話取出其他資料。</span><span class="sxs-lookup"><span data-stu-id="528be-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="528be-107">**取出其他事件追蹤資料**</span><span class="sxs-lookup"><span data-stu-id="528be-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="528be-108">透過呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)來啟動您的會話。</span><span class="sxs-lookup"><span data-stu-id="528be-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="528be-109">如需詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="528be-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="528be-110">呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 來設定其他事件追蹤資料。</span><span class="sxs-lookup"><span data-stu-id="528be-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="528be-111">使用 *ClassInformation* 參數中的 [**事件 \_ 資訊 \_ 類別**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)列舉來描述您想要取得的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="528be-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="528be-112">下列範例描述如何使用從 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)呼叫傳回的會話控制碼，以及來自 **事件 \_ 資訊 \_ 類別** 的 **TraceProviderBinaryTracking** 值，來呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)。</span><span class="sxs-lookup"><span data-stu-id="528be-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="528be-113">或者，您可以使用 [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) 來取得目前事件追蹤會話設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="528be-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="528be-114">如同 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)， [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) 會使用 [**EVENT \_ INFO \_ 類別**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) 列舉來描述要從系統中取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="528be-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
