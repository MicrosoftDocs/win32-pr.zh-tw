---
description: 建立群組組合和追蹤
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: 建立群組組合和追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846796"
---
# <a name="creating-groups-compositions-and-tracks"></a>建立群組組合和追蹤

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

群組、組合和軌跡是時間軸和來源剪輯之間的中繼層。 它們是由其可包含的物件類型所區分。

-   追蹤包含來源物件。
-   組合包含曲目和其他組合，但不包含來源物件。
-   群組是最上層的組合。 群組包含組合和追蹤，但組合不能包含群組。
-   *虛擬追蹤* 是可以位於組合或群組內的任何物件。 這包括追蹤和組合。

這些物件會公開下列介面：



| 介面                                                  | 公開者           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | 資料軌               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | 追蹤，組合 |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | 組合，群組 |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | 群組               |



 

這些介面包含將物件加入至時間軸的方法。

-   [**IAMTimeline：： AddGroup**](iamtimeline-addgroup.md)：將群組插入到時間軸。
-   [**IAMTimelineComp：： VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)：將虛擬追蹤插入組合或群組中。
-   [**IAMTimelineTrack：： SrcAdd**](iamtimelinetrack-srcadd.md)：將來源插入至追蹤。

例如，下列程式碼會將新的曲目插入群組中。 如上表所示，群組被視為一種組合，而曲目是一種虛擬追蹤。因此，若要將追蹤插入到群組中，您必須查詢其 **IAMTimelineComp** 介面的群組，並呼叫 **IAMTimelineComp：： VTrackInsBefore** 方法。


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



**VTrackInsBefore** 的第二個參數會指定虛擬追蹤的優先順序。優先權層級從零開始。 如果您指定的值是-1，則會在優先順序清單的結尾插入虛擬追蹤。 如果您指定的值已有虛擬追蹤，則從該點開始的所有專案都會依一個優先權層級向下移動。 請勿以大於虛擬追蹤數目的優先順序插入虛擬追蹤，因為它會導致未定義的行為。

若要從時間軸永久刪除物件，請呼叫物件上的 [**IAMTimelineObj：： RemoveAll**](iamtimelineobj-removeall.md) 。 這個方法會移除物件及其所有子系。 若要移除物件以在時間軸中的其他位置重新插入物件，請改為呼叫 [**IAMTimelineObj：： remove**](iamtimelineobj-remove.md) 。 不同于 **RemoveAll**，這個方法不會刪除物件的子系。 若要從時程表中移除所有專案，請呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 



