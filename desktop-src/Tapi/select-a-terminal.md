---
description: 下列程式碼範例示範如何在與呼叫相關聯的資料流程上選取終端機。
ms.assetid: ff43e81c-ff39-466d-870a-54b75c2938a4
title: 選取終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d195e021f5937c733f3d7a0efce0cfee5eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000201"
---
# <a name="select-a-terminal"></a><span data-ttu-id="d0466-103">選取終端機</span><span class="sxs-lookup"><span data-stu-id="d0466-103">Select a Terminal</span></span>

<span data-ttu-id="d0466-104">下列程式碼範例示範如何在與呼叫相關聯的資料流程上選取終端機。</span><span class="sxs-lookup"><span data-stu-id="d0466-104">The following code example demonstrates how to select terminals onto streams associated with a call.</span></span>

<span data-ttu-id="d0466-105">使用此程式碼範例之前，您必須先在 [初始化 TAPI](initialize-tapi.md) 中執行作業，然後 [選取位址](select-an-address.md)。</span><span class="sxs-lookup"><span data-stu-id="d0466-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="d0466-106">此外，此範例會要求應用程式已經有連入或撥出電話的 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d0466-106">Also, this example requires that the application already have a pointer to the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) interface of either an incoming or outgoing call.</span></span> <span data-ttu-id="d0466-107">如需如何取得此指標的程式碼範例，請參閱 [進行呼叫](make-a-call.md) 或 [接收呼叫](receive-a-call.md) 。</span><span class="sxs-lookup"><span data-stu-id="d0466-107">See [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) for code examples on how to obtain this pointer.</span></span>

> [!Note]  
> <span data-ttu-id="d0466-108">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="d0466-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pAddress is an ITAddress interface pointer.
// pBasicCall is an ITBasicCallControl interface pointer.

// Get the ITStreamControl interface.
ITStreamControl * pStreamControl;
HRESULT hr = pBasicCall->QueryInterface(
        IID_ITStreamControl,
        (void **) &pStreamControl
        );
// If ( hr != S_OK ) process the error here. 

// Enumerate the streams and select 
// terminals onto them.
IEnumStream * pEnumStreams;
ITStream    * pStream;
hr = pStreamControl->EnumerateStreams(&pEnumStreams);
// If ( hr != S_OK ) process the error here. 

while ( S_OK == pEnumStreams->Next(1, &pStream, NULL) )
{
    // Get the media type and direction of this stream.
    long                lMediaType;
    TERMINAL_DIRECTION  dir;
    hr = pStream->get_MediaType( &lMediaType );
    // If ( hr != S_OK ) process the error here. 
    hr = pStream->get_Direction( &dir );
    // If ( hr != S_OK ) process the error here. 

    // Create the default terminal for this media type and direction.
    //   If lMediaType == TAPIMEDIATYPE_VIDEO and
    //   dir == TD_RENDER, a dynamic video render terminal
    //   is required. Please see Incoming.cpp in 
    //   the samples section of the SDK. 
    // For all other terminals, get the default static terminal.
    ITTerminal * pTerminal;
    ITTerminalSupport * pTerminalSupport;
    hr = pAddress->QueryInterface( 
            IID_ITTerminalSupport, 
            (void **)&pTerminalSupport
         );
    // If ( hr != S_OK ) process the error here. 
    hr = pTerminalSupport->GetDefaultStaticTerminal(
            lMediaType,
            dir,
            pTerminal
         );
    // If ( hr != S_OK ) process the error here. 
    // Select the terminal on the stream.
    hr = pStream->SelectTerminal(pTerminal);
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="d0466-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0466-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0466-110">**ITAddress**</span><span class="sxs-lookup"><span data-stu-id="d0466-110">**ITAddress**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[<span data-ttu-id="d0466-111">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="d0466-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="d0466-112">**ITStreamControl**</span><span class="sxs-lookup"><span data-stu-id="d0466-112">**ITStreamControl**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[<span data-ttu-id="d0466-113">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="d0466-113">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="d0466-114">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="d0466-114">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="d0466-115">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="d0466-115">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[<span data-ttu-id="d0466-116">**ITTerminalSupport**</span><span class="sxs-lookup"><span data-stu-id="d0466-116">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
