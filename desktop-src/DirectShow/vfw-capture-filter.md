---
description: VFW Capture 篩選
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: VFW Capture 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1471f32ebc5cbb6d008de4abe59140b81a56b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983370"
---
# <a name="vfw-capture-filter"></a>VFW Capture 篩選

此篩選器適用于使用適用于 Windows 的影片的較舊影片捕獲硬體。

此篩選器有兩個輸出圖釘。 其中一個稱為「Capture」，另一個稱為「預覽」或「重迭」。



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | **IPersistPropertyBag**、 [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)、 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 **ISpecifyPropertyPages**、 [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 輸入 Pin 媒體類型                    | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 輸入 Pin 介面                     | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 輸出 Pin 媒體類型                   | Capture：媒體媒體 \_ 、MEDIASUBTYPE \_ Null、format \_ VideoInfoOverlay：媒體媒體 \_ 、MEDIASUBTYPE 重迭 \_ 、format \_ VideoInfo<br/> 預覽：媒體媒體 \_ 、MEDIASUBTYPE \_ Null、FORMAT \_ VideoInfo<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 輸出 Pin 介面                    | Capture Pin： [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)、 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)、 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)、 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)覆迭釘選： [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> 預覽 Pin： [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)、 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IKsPropertySet**](ikspropertyset.md)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| 篩選 CLSID                             | CLSID \_ VfwCapture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 屬性頁 CLSID                      | CLSID \_ CaptureProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 可執行檔                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [篩選準則分類](filter-categories.md) | CLSID \_ VideoInputDeviceCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>備註

雖然 capture 釘能公開 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面，但只有 **SetFormat** 和 **>iformatprovider.getformat** 方法會針對此介面執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 




