---
description: 下表描述可引發筆觸集合事件的執行緒。EventThreadsStrokesAddedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 StrokesAdded 事件，會在筆墨線程上引發。StrokesRemovedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 StrokesRemoved 事件，會在筆墨線程上引發。
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: 筆觸集合事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589778"
---
# <a name="strokes-collection-events"></a>筆觸集合事件

下表描述可引發 [**筆觸**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合事件的執行緒。



| 事件                                               | 執行緒                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**StrokesAdded**](inkstrokes-strokesadded.md)事件，會在筆墨線程上引發。<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**StrokesRemoved**](inkstrokes-strokesremoved.md)事件，會在筆墨線程上引發。<br/> |



 

 

 
