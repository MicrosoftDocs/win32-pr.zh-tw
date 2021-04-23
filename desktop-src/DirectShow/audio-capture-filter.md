---
description: 音訊捕獲篩選器
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: 音訊捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a630452565fafad3c4a4420154efd8fe6b282f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910206"
---
# <a name="audio-capture-filter"></a><span data-ttu-id="eb086-103">音訊捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="eb086-103">Audio Capture Filter</span></span>

<span data-ttu-id="eb086-104">音訊捕獲篩選器代表音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="eb086-104">The Audio Capture filter represents an audio capture device.</span></span> <span data-ttu-id="eb086-105">它有一個「捕獲輸出」釘選和數個輸入圖釘， (卡上的每一種輸入類型，例如線路輸入、Mic、CD 和 MIDI) 。</span><span class="sxs-lookup"><span data-stu-id="eb086-105">It has one capture output pin and several input pins (one for each type of input on the card, such as Line In, Mic, CD, and MIDI).</span></span>

<span data-ttu-id="eb086-106">此篩選器可以使用多個硬體裝置，因此呼叫 CoCreateInstance 來建立篩選器無法運作。</span><span class="sxs-lookup"><span data-stu-id="eb086-106">This filter can work with more than one hardware device, so calling CoCreateInstance to create the filter does not work.</span></span> <span data-ttu-id="eb086-107">相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="eb086-107">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="eb086-108">系統裝置列舉值會為每個裝置傳回唯一的標記。</span><span class="sxs-lookup"><span data-stu-id="eb086-108">The System Device Enumerator returns a unique moniker for each device.</span></span> <span data-ttu-id="eb086-109">標記的易記名稱會對應至裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb086-109">The moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="eb086-110"> (這是出現在 GraphEdit 中的名稱。 ) 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="eb086-110">(This is the name that appears in GraphEdit.) For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>



| <span data-ttu-id="eb086-111">標籤</span><span class="sxs-lookup"><span data-stu-id="eb086-111">Label</span></span> | <span data-ttu-id="eb086-112">值</span><span class="sxs-lookup"><span data-stu-id="eb086-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb086-113">篩選介面</span><span class="sxs-lookup"><span data-stu-id="eb086-113">Filter Interfaces</span></span>                        | <span data-ttu-id="eb086-114">[**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)、 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、IPersistPropertyBag、ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="eb086-114">[**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                               |
| <span data-ttu-id="eb086-115">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="eb086-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="eb086-116">媒體 \_ AnalogAudio、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="eb086-116">MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="eb086-117">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="eb086-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="eb086-118">[**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="eb086-118">[**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                           |
| <span data-ttu-id="eb086-119">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="eb086-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="eb086-120">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="eb086-120">MEDIATYPE\_Audio, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="eb086-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="eb086-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="eb086-122">[**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)、 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)、 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="eb086-122">[**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="eb086-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="eb086-123">Filter CLSID</span></span>                             | <span data-ttu-id="eb086-124">不適用</span><span class="sxs-lookup"><span data-stu-id="eb086-124">Not applicable</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="eb086-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="eb086-125">Property Page CLSID</span></span>                      | <span data-ttu-id="eb086-126">CLSID \_ AudioInputMixerProperties</span><span class="sxs-lookup"><span data-stu-id="eb086-126">CLSID\_AudioInputMixerProperties</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="eb086-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="eb086-127">Executable</span></span>                               | <span data-ttu-id="eb086-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="eb086-128">qcap.dll</span></span>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="eb086-129">優點</span><span class="sxs-lookup"><span data-stu-id="eb086-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="eb086-130">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="eb086-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="eb086-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="eb086-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="eb086-132">CLSID \_ AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="eb086-132">CLSID\_AudioInputDeviceCategory</span></span>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="eb086-133">備註</span><span class="sxs-lookup"><span data-stu-id="eb086-133">Remarks</span></span>

<span data-ttu-id="eb086-134">輸入圖釘代表實體硬體連線，而且永遠不會連接到 DirectShow 中的其他篩選器。</span><span class="sxs-lookup"><span data-stu-id="eb086-134">The input pins represent physical hardware connections and are never connected to other filters in DirectShow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb086-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb086-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb086-136">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="eb086-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="eb086-137">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="eb086-137">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



