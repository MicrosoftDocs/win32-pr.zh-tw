---
description: 具現化編解碼器 DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: 具現化編解碼器 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943400"
---
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="8d826-103">具現化編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="8d826-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="8d826-104">您可以藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM 函數來建立編解碼器。</span><span class="sxs-lookup"><span data-stu-id="8d826-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="8d826-105">您必須傳遞 SQL-DMO 的類別識別碼、 **IMediaObject** 的介面識別碼，以及指向 **IMediaObject** 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="8d826-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="8d826-106">編解碼器 DMOs 的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。</span><span class="sxs-lookup"><span data-stu-id="8d826-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="8d826-107">**IMediaObject** 介面識別碼的常數是 IID \_ IMediaObject。</span><span class="sxs-lookup"><span data-stu-id="8d826-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="8d826-108">下列程式碼範例示範如何建立編解碼器的實例：</span><span class="sxs-lookup"><span data-stu-id="8d826-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a><span data-ttu-id="8d826-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d826-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d826-110">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="8d826-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
