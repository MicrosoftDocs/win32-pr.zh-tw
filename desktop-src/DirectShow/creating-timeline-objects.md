---
description: 建立時間軸物件
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: 建立時間軸物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0a2a88b2cd931e6a9d12274f4a2503b4c97d52348b6ed2629c22bf204f302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054778"
---
# <a name="creating-timeline-objects"></a>建立時間軸物件

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本文中顯示的範例程式碼會以空白的時間軸開始，但如果您載入現有的專案，而且想要在其中新增物件，則適用相同的步驟。

若要在時間軸中建立任何類型的物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。 例如，下列程式碼會建立新的群組：


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



第二個參數是 [**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md) 列舉的成員。 它會指定要建立的時間軸物件類型，例如群組或曲目。

**CreateEmptyNode** 方法會建立物件，並傳回物件的 [**IAMTimelineObj**](iamtimelineobj.md)介面指標。 此外，它也會遞增 **IAMTimelineObj** 介面上的參考計數，因此您必須在使用完畢之後釋放介面。 請勿呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。 相反地，請一律使用 **CreateEmptyNode** 來建立時間軸物件，因為它會初始化要在時間軸中使用的新物件。

[**IAMTimelineObj**](iamtimelineobj.md)介面是泛型介面。 它提供所有類型時程表物件通用的方法。 每種類型的物件也會公開其他介面。 例如，群組會公開 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面，以及其他群組。 您可以藉由呼叫 **QueryInterface** 來取得其他介面的指標。

建立物件之後，它還不是時間軸的一部分。 將物件加入至時間軸的方法取決於物件類型。 下一節說明如何將群組、組合和追蹤新增至時間軸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 
