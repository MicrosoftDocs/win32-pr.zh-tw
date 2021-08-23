---
description: WDM 類別驅動程式篩選
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: WDM 類別驅動程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd93db09c638ed7a8a217bec28a565086dcbfcae2b5702c9e1d07778c338646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071892"
---
# <a name="wdm-class-driver-filters"></a>WDM 類別驅動程式篩選

如果捕捉裝置使用 Windows Driver Model (WDM) 驅動程式，則圖形可能需要來自 capture 篩選器的特定篩選準則。 這些篩選器稱為資料流程類別驅動程式篩選器或 WDM 篩選。 它們支援硬體所提供的其他功能。 例如，TV 調諧器介面卡具有設定通道的功能。 對應的篩選器是 [電視調諧器](tv-tuner-filter.md) 篩選器，它會公開 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) 介面。 若要將此功能提供給應用程式使用，您必須將電視調諧器篩選器連線到 capture 篩選器。

[**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面提供最簡單的方式，將 WDM 篩選器新增至圖形。 在建立圖形的某個時間點，呼叫 [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 或 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。 其中一種方法會自動找出必要的 WDM 篩選，並將其連接到 capture 篩選器。 本節的其餘部分將說明如何手動新增 WDM 篩選。 不過，請注意，建議的方法是直接呼叫其中一個 **ICaptureGraphBuilder2** 方法。

WDM 篩選器上的釘選支援一或多個媒體。 媒體定義通訊的方法，例如匯流排。 您必須連接支援相同媒體的釘選。 [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)結構相當於用於核心串流驅動程式的 **KSPIN \_ 中型** 結構，會定義 DirectShow 中的媒體。 **REGPINMEDIUM** 結構的 **clsMedium** 成員會為媒體指定 (CLSID) 的類別識別碼。 若要取出 pin 的媒體，請呼叫 [**IKsPin：： KsQueryMediums**](ikspin-ksquerymediums.md) 方法。 這個方法會傳回包含 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構之記憶體區塊的指標，後面接著零或多個 **REGPINMEDIUM** 結構。 每個 **REGPINMEDIUM** 結構都會識別 pin 所支援的媒體。

如果媒體具有 GUID \_ Null 或 KSMEDIUMSETID 標準的 CLSID，請勿連接 pin \_ 。 這些是預設值，表示 pin 不支援媒體。

此外，除非篩選只需要該 pin 的一個連接實例，否則請勿連接 pin。 否則，您的應用程式可能會嘗試連接不應該有連線的各種 pin，而這可能會造成程式停止回應。 若要找出所需的實例數目，請取出 KSPROPERTY \_ PIN \_ NECESSARYINSTANCES 屬性集，如下列程式碼範例所示。  (為了簡潔起見，此範例不會測試任何傳回碼或釋放任何介面。 當然，您的應用程式也應該這麼做。 ) 


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



下列虛擬程式碼是一個非常簡短的大綱，說明如何尋找及連接 WDM 篩選。 它會省略許多詳細資料，而且只是用來顯示應用程式需要採取的一般步驟。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> </dl>

 

 



