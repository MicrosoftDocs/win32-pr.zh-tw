---
description: Smart t 篩選
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart t 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a8e829d78658b867d3884240250c10d10a65c7cd309f109fe29b023c726518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964991"
---
# <a name="smart-tee-filter"></a>Smart t 篩選

影片捕獲圖形中會使用智慧 t a 濾波器，將影片串流分割成預覽資料流程和捕獲資料流程。 這是在沒有任何額外的資料複製的情況下完成。 輸出圖釘支援下游連線支援的任何媒體類型。

當影片捕獲篩選未提供個別的 pin 供捕捉和預覽時，智慧的 t a 濾波器會很有用。 只有在這種情況不會影響到捕捉效能時，智慧的 t 濾波器才會提供預覽資料。 它也會從預覽資料流程中移除時間戳記。 [Capture graph builder] 會在需要時自動插入智慧的 t a 濾波器。 如需詳細資訊，請參閱 [結合影片捕獲和預覽](combining-video-capture-and-preview.md)。

下圖顯示使用智慧型 t a 濾波器的一般 capture graph。

![使用智慧的 t a 濾波器](images/smarttee.png)



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                           |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                           |
| 輸出 Pin 介面                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ SmartTee                                                                                                |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                              |
| 可執行檔                               | qcap.dll                                                                                                       |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                            |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>備註

捕捉釘是輸出針腳0，而預覽 pin 則是輸出 pin 1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



