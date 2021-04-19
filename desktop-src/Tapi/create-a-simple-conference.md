---
description: 下列程式碼範例示範如何建立簡單的會議通話。 如需 IP 多播多媒體視訊會議的相關資訊，請參閱關於會合 IP 電話語音會議。
ms.assetid: fb55853d-b882-41c8-99e6-bfa897b2dabf
title: 建立簡單的會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa0bfd8fede9fa61aedb6b630a2451803e2257d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980542"
---
# <a name="create-a-simple-conference"></a><span data-ttu-id="3ae66-104">建立簡單的會議</span><span class="sxs-lookup"><span data-stu-id="3ae66-104">Create a Simple Conference</span></span>

<span data-ttu-id="3ae66-105">下列程式碼範例示範如何建立簡單的會議通話。</span><span class="sxs-lookup"><span data-stu-id="3ae66-105">The following code example demonstrates the creation of a simple conference call.</span></span> <span data-ttu-id="3ae66-106">如需 IP 多播多媒體視訊會議的相關資訊，請參閱 [關於會合 Ip 電話語音會議](about-rendezvous-ip-telephony-conferencing.md)。</span><span class="sxs-lookup"><span data-stu-id="3ae66-106">For information on IP multicast multimedia video conferencing, see [About Rendezvous IP Telephony Conferencing](about-rendezvous-ip-telephony-conferencing.md).</span></span>

<span data-ttu-id="3ae66-107">使用這個程式碼範例之前，必須先進行呼叫，而且您必須執行中的作業，再執行 [呼叫](make-a-call.md) 或 [接收呼叫](receive-a-call.md) 。</span><span class="sxs-lookup"><span data-stu-id="3ae66-107">Before using this code example, a call must be in progress, and you must perform the operations in [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) have been performed.</span></span>

> [!Note]  
> <span data-ttu-id="3ae66-108">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="3ae66-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// From elsewhere in your code, you have obtained pBasicCall and pCallInfo, 
// which are pointers to the ITBasicCallControl and ITCallInfo interfaces
// of a call currently in progress. pAddress is an ITAddress pointer.

// Create a consultation call for the conference.
ITBasicCallControl *pConsultCall;
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Move the consultation call into your conference.
// Note: If a CallHub object does not already exist, TAPI will create it.
hr = pBasicCall->Conference(
               pConsultCall,
               VARIANT_TRUE
               );
// If ( hr != S_OK ) process the error here. 

// Finish the creation of the conference.
hr = pConsultCall->Finish(FM_ASCONFERENCE);
// If ( hr != S_OK ) process the error here. 

// Assuming the Finish method succeeds, the consultation call (pConsultCall)
// may transition to the CS_DISCONNECTED state or may remain connected, 
// depending on the service provider.
//
// Get the ITCallHub interface pointer.
ITCallHub *pCallHub;
hr = pCallInfo->get_CallHub( pCallHub );
// If ( hr != S_OK ) process the error here. 

// You can use the ITCallHub interface to obtain additional information on
// the conference. Specific capabilities depend on the TSP/MSP being used.
```

## <a name="related-topics"></a><span data-ttu-id="3ae66-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ae66-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ae66-110">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="3ae66-110">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="3ae66-111">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="3ae66-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="3ae66-112">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="3ae66-112">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



