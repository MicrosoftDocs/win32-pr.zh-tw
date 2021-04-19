---
description: 下列程式碼範例示範如何建立呼叫物件、探索與呼叫相關聯的資料流程、選取和建立適當的終端機、選取資料流程上的終端機，以及完成連接。
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: 撥打電話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978879"
---
# <a name="make-a-call"></a><span data-ttu-id="de3f3-103">撥打電話</span><span class="sxs-lookup"><span data-stu-id="de3f3-103">Make a Call</span></span>

<span data-ttu-id="de3f3-104">下列程式碼範例示範如何建立呼叫物件、探索與呼叫相關聯的資料流程、選取和建立適當的終端機、選取資料流程上的終端機，以及完成連接。</span><span class="sxs-lookup"><span data-stu-id="de3f3-104">The following code example demonstrates how to create a call object, discover the streams associated with the call, select and create appropriate terminals, select the terminals onto the streams, and complete the connection.</span></span>

<span data-ttu-id="de3f3-105">使用此程式碼範例之前，您必須先在 [初始化 TAPI](initialize-tapi.md) 中執行作業，然後 [選取位址](select-an-address.md)。</span><span class="sxs-lookup"><span data-stu-id="de3f3-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="de3f3-106">此外，您必須在呼叫 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)之後，執行 [選取終端](select-a-terminal.md)機中說明的作業。</span><span class="sxs-lookup"><span data-stu-id="de3f3-106">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the call to [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span></span>

> [!Note]  
> <span data-ttu-id="de3f3-107">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="de3f3-107">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a><span data-ttu-id="de3f3-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="de3f3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de3f3-109">**ITAddress::CreateCall**</span><span class="sxs-lookup"><span data-stu-id="de3f3-109">**ITAddress::CreateCall**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[<span data-ttu-id="de3f3-110">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="de3f3-110">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="de3f3-111">**ITBasicCallControl：： Connect**</span><span class="sxs-lookup"><span data-stu-id="de3f3-111">**ITBasicCallControl::Connect**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



