---
description: '下表描述筆墨物件事件可以引發的執行緒。EventThreadsInkAddedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 InkAdded 事件，會在筆墨線程上引發。InkDeletedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 InkDeleted 事件，會在筆墨線程上引發。 '
ms.assetid: 410f7126-5c4c-4c0c-8aa6-c94f15c903fc
title: 筆墨物件事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63217f603b06703b7824c19d3a709fdb97f31c9890e3148a6eeefd1e681d63b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451935"
---
# <a name="ink-object-events"></a>筆墨物件事件

下表描述 [**筆墨**](inkdisp-class.md) 物件事件可以引發的執行緒。



| 事件                                    | 執行緒                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**InkAdded**](inkdisp-inkadded.md)事件，會在筆墨線程上引發。<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**InkDeleted**](inkdisp-inkdeleted.md)事件，會在筆墨線程上引發。<br/> |



 

 

 




