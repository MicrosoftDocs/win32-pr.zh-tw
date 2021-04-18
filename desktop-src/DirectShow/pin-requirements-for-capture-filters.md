---
description: 本主題說明在 DirectShow 捕獲篩選器上執行輸出 pin 的需求。
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: 捕獲篩選準則的 Pin 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971279"
---
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="db115-103">捕獲篩選準則的 Pin 需求</span><span class="sxs-lookup"><span data-stu-id="db115-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="db115-104">本主題說明在 DirectShow 捕獲篩選器上執行輸出 pin 的需求。</span><span class="sxs-lookup"><span data-stu-id="db115-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="db115-105">接腳名稱</span><span class="sxs-lookup"><span data-stu-id="db115-105">Pin Name</span></span>

<span data-ttu-id="db115-106">您可以為 pin 提供任何名稱。</span><span class="sxs-lookup"><span data-stu-id="db115-106">You can give a pin any name.</span></span> <span data-ttu-id="db115-107">如果 pin 名稱以波狀符號 (~) 字元開頭，則當應用程式呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)時，篩選圖形管理員不會自動轉譯該 pin。</span><span class="sxs-lookup"><span data-stu-id="db115-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="db115-108">例如，如果篩選具有 capture pin 和預覽 pin，您可以分別將它們命名為 "~ Capture" 和 "Preview"。</span><span class="sxs-lookup"><span data-stu-id="db115-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="db115-109">如果應用程式在圖形中轉譯該篩選，預覽 pin 將會連接到其預設轉譯器，而不會連接到捕捉釘選，這是合理的預設行為。</span><span class="sxs-lookup"><span data-stu-id="db115-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="db115-110">這也適用于傳遞不打算轉譯之資訊資料的 pin，或需要設定自訂屬性的釘選。</span><span class="sxs-lookup"><span data-stu-id="db115-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="db115-111">請注意，應用程式仍然可以手動連接具有波狀符號 (~) 前置詞的釘選。</span><span class="sxs-lookup"><span data-stu-id="db115-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="db115-112">釘選類別</span><span class="sxs-lookup"><span data-stu-id="db115-112">Pin Category</span></span>

<span data-ttu-id="db115-113">捕捉篩選準則一律具有 capture pin，而且可能有預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="db115-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="db115-114">某些 capture 篩選器可能會有其他輸出圖釘，以提供其他類型的資料，例如控制資訊。</span><span class="sxs-lookup"><span data-stu-id="db115-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="db115-115">每個輸出圖釘都必須公開 [**IKsPropertySet**](ikspropertyset.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="db115-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="db115-116">應用程式會使用此介面來判斷釘選類別。</span><span class="sxs-lookup"><span data-stu-id="db115-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="db115-117">Pin 通常會傳回 PIN \_ 類別 \_ 捕獲或 pin \_ 類別 \_ 預覽。</span><span class="sxs-lookup"><span data-stu-id="db115-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="db115-118">如需詳細資訊，請參閱 [釘選屬性集](pin-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="db115-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="db115-119">下列範例顯示如何執行 [**IKsPropertySet**](ikspropertyset.md) ，以傳回捕捉釘選上的釘選類別：</span><span class="sxs-lookup"><span data-stu-id="db115-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="db115-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="db115-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db115-121">寫入捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="db115-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



