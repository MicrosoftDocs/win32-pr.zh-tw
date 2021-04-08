---
description: 音訊捕獲篩選器
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: 音訊捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688307"
---
# <a name="audio-capture-filter"></a>音訊捕獲篩選器

音訊捕獲篩選器代表音訊捕獲裝置。 它有一個「捕獲輸出」釘選和數個輸入圖釘， (卡上的每一種輸入類型，例如線路輸入、Mic、CD 和 MIDI) 。

此篩選器可以使用多個硬體裝置，因此呼叫 CoCreateInstance 來建立篩選器無法運作。 相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。 系統裝置列舉值會為每個裝置傳回唯一的標記。 標記的易記名稱會對應至裝置的名稱。  (這是出現在 GraphEdit 中的名稱。 ) 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)、 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、IPersistPropertyBag、ISpecifyPropertyPages                                                               |
| 輸入 Pin 媒體類型                    | 媒體 \_ AnalogAudio、MEDIASUBTYPE \_ Null                                                                                                                                                                                                                                                         |
| 輸入 Pin 介面                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                                                                               |
| 輸出 Pin 介面                    | [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)、 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)、 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | 不適用                                                                                                                                                                                                                                                                                     |
| 屬性頁 CLSID                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| 可執行檔                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

輸入圖釘代表實體硬體連線，而且永遠不會連接到 DirectShow 中的其他篩選器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[音訊捕獲](audio-capture.md)
</dt> </dl>

 

 



