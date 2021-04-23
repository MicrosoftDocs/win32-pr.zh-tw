---
description: 電視調諧器篩選器
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: 電視調諧器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909026"
---
# <a name="tv-tuner-filter"></a>電視調諧器篩選器

電視調諧器篩選器會選取要查看的類比廣播或纜線頻道。 單一輸出資料流程是類比基帶影片的硬體路徑。 此輸出應該連接到類比視頻縱橫條篩選器。 輸入 pin 包含纜線和天線輸入的輸入。



| 標籤 | 值 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner)、 **ISpecifyPropertyPages**、 **IPersistPropertyBag**、 **IKsObject**、 [**IKsPropertySet**](ikspropertyset.md) |
| 輸入 Pin 媒體類型                    | 不適用。                                                                                                                                                                   |
| 輸入 Pin 介面                     | 不適用。                                                                                                                                                                   |
| 輸出 Pin 媒體類型                   | 影片：媒體 \_ 類型 AnalogVideo、KSDATAFORMAT \_ 子類型 \_ NONE 音訊：媒體類型 \_ AnalogAudio、MEDIASUBTYPE \_ Null                                                                      |
| 輸出 Pin 介面                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| 篩選 CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| 屬性頁 CLSID                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| 可執行檔                               | KSTVTune.ax                                                                                                                                                                       |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                               |
| [篩選準則分類](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



