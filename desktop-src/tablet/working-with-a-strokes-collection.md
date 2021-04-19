---
description: 分割物件所分析的筆劃集合會保留在分隔物件的 [筆劃] 屬性中。
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: 使用筆劃集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdeb03ce8168cec489dfed954a091f50f8d846d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966706"
---
# <a name="working-with-a-strokes-collection"></a>使用筆劃集合

[**分割**](inkdivider-class.md)物件所分析的 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合會保留在 **分隔** 物件的 [[**筆劃**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)] 屬性中。 因為 **筆劃** 集合是筆墨資料的參考，而不是實際資料本身，所以 **筆劃** 集合的父 [**筆墨**](inkdisp-class.md)物件變更可能會使 **筆劃** 集合無效。 如需筆墨資料的詳細資訊，請參閱 [筆墨資料](ink-data.md)。 如需筆跡集合的詳細資訊，請參閱 [筆墨收集](ink-collection.md)。

若要讓 [**分隔**](inkdivider-class.md)物件的 [**筆觸**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)屬性與 [**Ink**](inkdisp-class.md)物件保持同步，請使用 **ink** 物件的 [**InkAdded**](inkdisp-inkadded.md)和 [**InkDeleted**](inkdisp-inkdeleted.md)事件，來接聽應該在 **分隔** 物件中新增或移除的筆劃。 這涵蓋了在 **筆跡** 物件中新增、刪除、裁剪或分割筆劃的情況。 在 **筆跡** 物件中移動、縮放或其他筆劃的轉換不會產生 **InkAdded** 或 **InkDeleted** 事件。 若要在 **分割** 物件的 [**筆觸**] 屬性中反映這類轉換，請在 [**分隔線**] 物件的筆觸上執行相同的轉換。

[**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)物件的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)屬性會在建立 **DivisionResult** 物件時，于 [**分割**](inkdivider-class.md)物件中包含一份筆劃。 您可以比較兩個 **DivisionResult** 物件的 **筆觸** 屬性，判斷筆劃是否已在呼叫 [**除法**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide)方法的兩倍之間變更。

[**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)物件的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes)屬性包含 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)物件中對應至這個專案之筆劃的子集。 您可以將這些筆觸傳遞給個別的 [**RecognizerCoNtext**](inkrecognizercontext-class.md) ，以取得元素的辨識結果。 由於手寫元素存在於不同的詳細資料層級，因此不同元素的 [**筆觸**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合可能會重迭。 例如，辨識區段元素的 **筆觸** 集合將會是辨識區段所屬之線條元素的 **筆觸** 集合子集。

 

 
