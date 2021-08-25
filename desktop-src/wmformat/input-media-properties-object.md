---
title: 輸入媒體屬性物件
description: 輸入媒體屬性物件
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows媒體格式 SDK、輸入媒體屬性物件
- Advanced Systems Format (ASF) 、輸入媒體屬性物件
- ASF (Advanced 系統格式) 、輸入媒體屬性物件
- 物件、輸入媒體屬性物件
- 輸入媒體屬性物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf5fac14de1c0fdc6619ab0dfe61feb9fcf577acb5c22dc2243a96d943921c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809028"
---
# <a name="input-media-properties-object"></a>輸入媒體屬性物件

寫入器物件所建立的輸入媒體屬性物件支援下列介面。 這些介面是透過對寫入器物件之其中一個介面的 **QueryInterface** 呼叫來存取。



| 介面                                        | 描述                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | 捕獲輸入資料流程的屬性。                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | 用作其他媒體屬性介面的基底介面， (輸入、輸出和影片) 。             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | 管理影片資料流程的屬性。 這是選擇性的介面，僅適用于影片串流。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**寫入器物件**](writer-object.md)
</dt> </dl>

 

 




