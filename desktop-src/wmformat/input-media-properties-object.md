---
title: 輸入媒體屬性物件
description: 輸入媒體屬性物件
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK、輸入媒體屬性物件
- Advanced Systems Format (ASF) 、輸入媒體屬性物件
- ASF (Advanced 系統格式) 、輸入媒體屬性物件
- 物件、輸入媒體屬性物件
- 輸入媒體屬性物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841880"
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

 

 




