---
description: 時間軸物件
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: 時間軸物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998002"
---
# <a name="timeline-objects"></a>時間軸物件

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

時間軸中的每種物件類型（來源、追蹤、效果等等）都是不同的 COM 物件。 不過，應用程式不會使用 **CoCreateInstance** 函數來建立它們。 相反地，它會呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。 這個方法會建立所要求型別的物件、將它初始化，然後將指標傳回物件。 如需詳細資訊，請參閱 [建立時間軸](constructing-a-timeline.md)。

每個時間軸物件都會公開 [**IAMTimelineObj**](iamtimelineobj.md) 介面。 此外，各種物件類型都支援其專屬的特殊介面：

-   來源： [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   追蹤： [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   組合： [ **IAMTimelineComp**](iamtimelinecomp.md)
-   群組： [**IAMTimelineComp**](iamtimelinecomp.md)、 [**IAMTimelineGroup**](iamtimelinegroup.md)
-   效果： [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   轉換： [ **IAMTimelineTrans**](iamtimelinetrans.md)

請注意，群組是一種組合，因此支援 [**IAMTimelineComp**](iamtimelinecomp.md)，以及自己的 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面。

除了先前所列的介面之外，時程表物件也會公開其他的次要介面。 這些介面會決定物件類型之間的關聯性。



| 介面                                                  | 意義                                                                                                       | 公開者                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | 此物件是虛擬追蹤。虛擬追蹤可以位於組合內，並保留其他時程表物件。 | 撰寫、追蹤                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | 物件可能會有效果。                                                                                  | 撰寫、追蹤、來源        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | 物件可以有轉換。                                                                              | 撰寫、追蹤                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | 物件可以分割成兩個物件。                                                                     | 追蹤、來源、效果、轉換 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[時間軸元件的總覽](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



