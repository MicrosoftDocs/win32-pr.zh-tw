---
description: 列舉媒體類型
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: 列舉媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909c25e9ae5f90a3084eebb531431cc93ef46cd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321532"
---
# <a name="enumerating-media-types"></a><span data-ttu-id="b7cd7-103">列舉媒體類型</span><span class="sxs-lookup"><span data-stu-id="b7cd7-103">Enumerating Media Types</span></span>

<span data-ttu-id="b7cd7-104">Pin 支援 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，其會列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-104">Pins support the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method, which enumerates a pin's preferred media types.</span></span> <span data-ttu-id="b7cd7-105">它會傳回 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-105">It returns a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="b7cd7-106">[**IEnumMediaTypes：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next)方法會取出描述媒體類型的 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構指標。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-106">The [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method retrieves pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures describing media types.</span></span>

<span data-ttu-id="b7cd7-107">媒體類型列舉值主要是用來協助篩選圖形管理員進行智慧型連接，而您的應用程式可能不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-107">The media type enumerator exists primarily to help the Filter Graph Manager make intelligent connections, and your applications will probably not use it.</span></span> <span data-ttu-id="b7cd7-108">Pin 不一定會傳回任何慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-108">A pin does not necessarily return any preferred media types.</span></span> <span data-ttu-id="b7cd7-109">此外，它所傳回的媒體類型可能取決於篩選器的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-109">Moreover, the media types it returns might depend on the filter's connection status.</span></span> <span data-ttu-id="b7cd7-110">例如，篩選的輸出圖釘可能會傳回一組不同的媒體類型，取決於針對篩選器輸入 pin 所設定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-110">For example, a filter's output pin might return a different set of media types depending on which media type was set for the filter's input pin.</span></span>

<span data-ttu-id="b7cd7-111">下列範例會尋找符合指定之主要類型、子類型或格式類型的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-111">The following example finds a preferred media type that matches a specified major type, subtype, or format type.</span></span>


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="b7cd7-112">此範例會使用 [SafeRelease](/windows/desktop/medfound/saferelease) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="b7cd7-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b7cd7-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7cd7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7cd7-114">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="b7cd7-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="b7cd7-115">**IEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b7cd7-115">**IEnumMediaTypes**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
