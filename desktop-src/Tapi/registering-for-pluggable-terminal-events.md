---
description: 當資料流程選取終端機時，就會發生事件註冊程式。
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: 註冊可插入的終端機事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853080"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="e17cb-103">註冊可插入的終端機事件</span><span class="sxs-lookup"><span data-stu-id="e17cb-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="e17cb-104">當資料流程選取終端機時，就會發生事件註冊程式。</span><span class="sxs-lookup"><span data-stu-id="e17cb-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="e17cb-105">在終端機應用程式的 [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) 方法執行中，我們可以使用已附加至資料流程的終端機 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面，然後呼叫 **QueryInterface** 來尋找 [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)。</span><span class="sxs-lookup"><span data-stu-id="e17cb-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="e17cb-106">如果 **QueryInterface** 呼叫成功，我們可以呼叫 [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) 方法。</span><span class="sxs-lookup"><span data-stu-id="e17cb-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="e17cb-107">基於這個目的，我們應該建立可執行 [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="e17cb-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="e17cb-108">我們會將此介面傳遞為 **RegisterSink** 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="e17cb-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="e17cb-109">執行 [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) 呼叫的終端機將會儲存介面。</span><span class="sxs-lookup"><span data-stu-id="e17cb-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="e17cb-110">當終端機將會引發事件時，將會使用指標。</span><span class="sxs-lookup"><span data-stu-id="e17cb-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="e17cb-111">您可以使用 [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink)取消註冊事件接收器。</span><span class="sxs-lookup"><span data-stu-id="e17cb-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
