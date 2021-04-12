---
description: 具現化編解碼器 MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: 具現化編解碼器 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191439"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="1ff98-103">具現化編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="1ff98-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="1ff98-104">[媒體基礎轉換](media-foundation-transforms.md) (MFTs) 是執行 [**IMFTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="1ff98-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="1ff98-105">MFT 是一種物件，可將多媒體資料轉換為管線的一部分。</span><span class="sxs-lookup"><span data-stu-id="1ff98-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="1ff98-106">管線是由媒體來源、媒體轉換和媒體接收所組成的有向非循環圖表。</span><span class="sxs-lookup"><span data-stu-id="1ff98-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="1ff98-107">管線會以非同步方式處理串流處理多媒體資料。</span><span class="sxs-lookup"><span data-stu-id="1ff98-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="1ff98-108">雖然 MFTs 可具現化並獨立于媒體基礎管線基礎結構之外使用，但最好盡可能使用 MediaFoundation 架構。</span><span class="sxs-lookup"><span data-stu-id="1ff98-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="1ff98-109">您可以藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立編解碼器 MFT。</span><span class="sxs-lookup"><span data-stu-id="1ff98-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="1ff98-110">您必須傳遞 MFT 的類別識別碼、 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)的介面識別碼，以及指向 **IMFTransform** 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="1ff98-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="1ff98-111">編解碼器 MFTs 的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。</span><span class="sxs-lookup"><span data-stu-id="1ff98-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="1ff98-112">[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面識別碼的常數是 IID \_ IMFTransform。</span><span class="sxs-lookup"><span data-stu-id="1ff98-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="1ff98-113">下列程式碼範例示範如何建立編解碼器 MFT 的實例：</span><span class="sxs-lookup"><span data-stu-id="1ff98-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="1ff98-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ff98-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ff98-115">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="1ff98-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
