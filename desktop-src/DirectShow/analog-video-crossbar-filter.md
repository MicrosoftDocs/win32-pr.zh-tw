---
description: 類比視頻縱橫條篩選
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: 類比視頻縱橫條篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909596"
---
# <a name="analog-video-crossbar-filter"></a>類比視頻縱橫條篩選

類比視頻縱橫條篩選器表示影片啟用裝置上的一種影片，可支援 Windows Driver Model (WDM) 。

此篩選器是在 WDM 串流裝置上 crossbars 的包裝函式篩選。 篩選的易記名稱取自裝置。 每個輸出圖釘都代表類比基帶影片的硬體路徑。 其中一個輸入針腳是電視調諧器 ([Tv 調諧器篩選器](tv-tuner-filter.md)) 。 其他輸入 pin 支援影片或音訊串流。 篩選準則支援下游連接所支援的任何媒體子類型和格式。

您無法使用 CoCreateInstance 直接建立此篩選器。 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面會視需要自動將此篩選新增至圖形。

如需包裝函式篩選和 WDM 串流裝置的詳細資訊，請參閱 [硬體裝置如何參與篩選圖形](how-hardware-devices-participate-in-the-filter-graph.md)。



| 標籤 | 值 |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)、ISpecifyPropertyPages、IPersistPropertyBag、IPersistStream |
| 輸入 Pin 媒體類型                    | 媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo                                                 |
| 輸入 Pin 介面                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| 輸出 Pin 媒體類型                   | 媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo                                                 |
| 輸出 Pin 介面                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| 篩選 CLSID                             | 不適用                                                                                 |
| 屬性頁 CLSID                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| 可執行檔                               | ksxbar.ax                                                                                      |
| [優點](merit.md)                       | 驅動程式相依。                                                                              |
| [篩選準則分類](filter-categories.md) | AM \_ KSCATEGORY \_ 縱橫                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[使用 Crossbars](working-with-crossbars.md)
</dt> </dl>

 

 



