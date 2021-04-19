---
description: 下表描述可引發筆觸集合事件的執行緒。EventThreadsStrokesAddedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 StrokesAdded 事件，會在筆墨線程上引發。StrokesRemovedFires 筆墨線程或呼叫端執行緒上的。使用者與 InkCollector 物件、InkOverlay 物件或 InkPicture 控制項互動所產生的 StrokesRemoved 事件，會在筆墨線程上引發。
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: 筆觸集合事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978186"
---
# <a name="strokes-collection-events"></a>筆觸集合事件

下表描述可引發 [**筆觸**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合事件的執行緒。



| 事件                                               | 執行緒                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**StrokesAdded**](inkstrokes-strokesadded.md)事件，會在筆墨線程上引發。<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | 在筆跡執行緒或呼叫端的執行緒上引發。<br/> 使用者與 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項互動所產生的 [**StrokesRemoved**](inkstrokes-strokesremoved.md)事件，會在筆墨線程上引發。<br/> |



 

 

 
