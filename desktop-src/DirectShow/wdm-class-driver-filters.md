---
description: WDM 類別驅動程式篩選
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: WDM 類別驅動程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848429"
---
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="0f98d-103">WDM 類別驅動程式篩選</span><span class="sxs-lookup"><span data-stu-id="0f98d-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="0f98d-104">如果捕捉裝置使用 Windows Driver Model (WDM) 驅動程式，則圖形可能需要來自 capture 篩選器的特定篩選準則。</span><span class="sxs-lookup"><span data-stu-id="0f98d-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="0f98d-105">這些篩選器稱為資料流程類別驅動程式篩選器或 WDM 篩選。</span><span class="sxs-lookup"><span data-stu-id="0f98d-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="0f98d-106">它們支援硬體所提供的其他功能。</span><span class="sxs-lookup"><span data-stu-id="0f98d-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="0f98d-107">例如，TV 調諧器介面卡具有設定通道的功能。</span><span class="sxs-lookup"><span data-stu-id="0f98d-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="0f98d-108">對應的篩選器是 [電視調諧器](tv-tuner-filter.md) 篩選器，它會公開 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) 介面。</span><span class="sxs-lookup"><span data-stu-id="0f98d-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="0f98d-109">若要將此功能提供給應用程式使用，您必須將電視調諧器篩選器連線到 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="0f98d-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="0f98d-110">[**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面提供最簡單的方式，將 WDM 篩選器新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="0f98d-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="0f98d-111">在建立圖形的某個時間點，呼叫 [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 或 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。</span><span class="sxs-lookup"><span data-stu-id="0f98d-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="0f98d-112">其中一種方法會自動找出必要的 WDM 篩選，並將其連接到 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="0f98d-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="0f98d-113">本節的其餘部分將說明如何手動新增 WDM 篩選。</span><span class="sxs-lookup"><span data-stu-id="0f98d-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="0f98d-114">不過，請注意，建議的方法是直接呼叫其中一個 **ICaptureGraphBuilder2** 方法。</span><span class="sxs-lookup"><span data-stu-id="0f98d-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="0f98d-115">WDM 篩選器上的釘選支援一或多個媒體。</span><span class="sxs-lookup"><span data-stu-id="0f98d-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="0f98d-116">媒體定義通訊的方法，例如匯流排。</span><span class="sxs-lookup"><span data-stu-id="0f98d-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="0f98d-117">您必須連接支援相同媒體的釘選。</span><span class="sxs-lookup"><span data-stu-id="0f98d-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="0f98d-118">[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)結構（相當於用於核心串流驅動程式的 **KSPIN \_ 媒體** 結構）會定義 DirectShow 中的媒體。</span><span class="sxs-lookup"><span data-stu-id="0f98d-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="0f98d-119">**REGPINMEDIUM** 結構的 **clsMedium** 成員會為媒體指定 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f98d-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="0f98d-120">若要取出 pin 的媒體，請呼叫 [**IKsPin：： KsQueryMediums**](ikspin-ksquerymediums.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0f98d-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="0f98d-121">這個方法會傳回包含 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構之記憶體區塊的指標，後面接著零或多個 **REGPINMEDIUM** 結構。</span><span class="sxs-lookup"><span data-stu-id="0f98d-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="0f98d-122">每個 **REGPINMEDIUM** 結構都會識別 pin 所支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="0f98d-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="0f98d-123">如果媒體具有 GUID \_ Null 或 KSMEDIUMSETID 標準的 CLSID，請勿連接 pin \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f98d-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="0f98d-124">這些是預設值，表示 pin 不支援媒體。</span><span class="sxs-lookup"><span data-stu-id="0f98d-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="0f98d-125">此外，除非篩選只需要該 pin 的一個連接實例，否則請勿連接 pin。</span><span class="sxs-lookup"><span data-stu-id="0f98d-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="0f98d-126">否則，您的應用程式可能會嘗試連接不應該有連線的各種 pin，而這可能會造成程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="0f98d-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="0f98d-127">若要找出所需的實例數目，請取出 KSPROPERTY \_ PIN \_ NECESSARYINSTANCES 屬性集，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="0f98d-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="0f98d-128"> (為了簡潔起見，此範例不會測試任何傳回碼或釋放任何介面。</span><span class="sxs-lookup"><span data-stu-id="0f98d-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="0f98d-129">當然，您的應用程式也應該這麼做。 ) </span><span class="sxs-lookup"><span data-stu-id="0f98d-129">Your application should do both, of course.)</span></span>


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



<span data-ttu-id="0f98d-130">下列虛擬程式碼是一個非常簡短的大綱，說明如何尋找及連接 WDM 篩選。</span><span class="sxs-lookup"><span data-stu-id="0f98d-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="0f98d-131">它會省略許多詳細資料，而且只是用來顯示應用程式需要採取的一般步驟。</span><span class="sxs-lookup"><span data-stu-id="0f98d-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a><span data-ttu-id="0f98d-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f98d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f98d-133">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="0f98d-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



