---
description: 下列程式碼範例將示範來電轉接。
ms.assetid: 05862605-2600-4cdf-8390-e24e4e8586f3
title: 傳送通話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1d537efd33ea2df4ddb9ad3e9b55b633cca18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987290"
---
# <a name="transfer-a-call"></a><span data-ttu-id="2c5af-103">傳送通話</span><span class="sxs-lookup"><span data-stu-id="2c5af-103">Transfer a Call</span></span>

<span data-ttu-id="2c5af-104">下列程式碼範例將示範來電轉接。</span><span class="sxs-lookup"><span data-stu-id="2c5af-104">The following code example demonstrates a call transfer.</span></span>

<span data-ttu-id="2c5af-105">使用這個程式碼範例之前，必須先進行呼叫，而且您必須在 [呼叫](make-a-call.md) 中執行作業或 [接收呼叫](receive-a-call.md)。</span><span class="sxs-lookup"><span data-stu-id="2c5af-105">Before using this code example, a call must be in progress, and you must perform the operations in [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md).</span></span>

> [!Note]  
> <span data-ttu-id="2c5af-106">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="2c5af-106">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// From elsewhere in your code, you have obtained pAddress and pBasicCall, 
// which are pointers to the ITAddress and ITBasicCallControl interfaces
// of the call in progress that will be transferred.

// Create the call object for transfer. bstrAddressToCall and dwAddressType
// have been retrieved from a UI.
ITBasicCallControl * pConsultCall
HRESULT hr = pAddress->CreateCall(
        bstrAddressToCall,
        dwAddressType,
        &pConsultCall
        );
// If ( hr != S_OK ) process the error here. 

// Start the transfer.
hr = pBasicCall->Transfer(
        pConsultCall,
        VARIANT_TRUE
        );
// If ( hr != S_OK ) process the error here. 

// Depending on the service provider, additional operations may be available
// or required.

// Finish the transfer.
hr = pConsultCall->Finish(FM_ASTRANSFER);
// If ( hr != S_OK ) process the error here. 

// The consultation call transitions to CS_DISCONNECTED.
// The objects associated with pConsultCall and pBasicCall can be released immediately or
// used for information purposes and released later.
```

## <a name="related-topics"></a><span data-ttu-id="2c5af-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c5af-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c5af-108">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="2c5af-108">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="2c5af-109">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="2c5af-109">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="2c5af-110">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="2c5af-110">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)
</dt> </dl>

 

 



