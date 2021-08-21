---
description: AVI 壓縮程式篩選
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI 壓縮程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159270"
---
# <a name="avi-compressor-filter"></a>AVI 壓縮程式篩選

AVI 壓縮程式篩選器可讓影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器來聯結篩選圖形。 每個編解碼器都會顯示為篩選準則的個別實例。 您無法使用 CoCreateInstance 直接建立此篩選器。 相反地，您必須使用系統裝置枚舉器。 如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

篩選器的輸入 pin 會連接至輸出未壓縮影片資料的篩選器，例如影片捕獲篩選器或 [AVI 分隔器篩選器](avi-splitter-filter.md)。 篩選器的輸出圖釘通常會連接到 MUX 篩選器，例如 [AVI Mux 篩選器](avi-mux-filter.md)。

如果編解碼器支援舊樣式的 VFW 設定對話方塊或 [關於] 對話方塊，則應用程式可以使用 [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) 介面來顯示它。

> [!Note]  
> MPEG 壓縮機絕不會實作為 bc-vcm-lvm-hyperv 編解碼器，而只會實作為原生 DirectShow 篩選。

 



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、IPersistPropertyBag、ISpecifyPropertyPages                                                                                                             |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| 輸出 Pin 介面                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | 不適用                                                                                                                                                                                                                                     |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                                                                                                                  |
| 可執行檔                               | qcap.dll                                                                                                                                                                                                                                           |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



