---
description: DivisionUnit 物件代表 DivisionResult 物件的單一結構化元素。 DivisionUnit 物件可能代表繪圖、手寫的單一辨識區段、手寫行或手寫區塊。
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: 使用 DivisionUnit 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c2ce09bf2b67f5724bba523219d0555063c3f7215810d3b11c48596f979fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966507"
---
# <a name="working-with-the-divisionunit-object"></a>使用 DivisionUnit 物件

**DivisionUnit** 物件代表 **DivisionResult** 物件的單一結構化元素。 **DivisionUnit** 物件可能代表繪圖、手寫的單一辨識區段、手寫行或手寫區塊。

[**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉會定義版面配置分析可辨識的結構化元素類型。 在自動化中， **DivisionUnit** 物件稱為 [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit)。

**DivisionUnit** 物件的 [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype)屬性會傳回 **DivisionUnit** 物件為的結構化元素類型。 **DivisionUnit** 物件的 [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85))屬性會傳回手寫專案的辨識文字，或針對繪圖元素傳回 **Null** 。

**DivisionUnit** 物件的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes)屬性包含 **DivisionResult** 物件中對應至這個專案之筆劃的子集。 由於手寫元素存在於不同層級的詳細資料，因此不同元素的 **筆觸** 集合可能會重迭。 具體而言，辨識區段會共用含有線條和區塊的筆劃，而線條則會與它所屬的區塊共用筆觸。

**DivisionUnit** 物件的 [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform)屬性會傳回將元素的筆觸旋轉為水準的矩陣。 若為段落和繪圖元素， **RotationTransform** 屬性會傳回識別矩陣。 文字辨識器在手寫上的執行速度會比在手寫上進行水準對齊的方式更好。 在自動化中，這稱為 **RotationTransform** 屬性，它會傳回包含轉換矩陣的 [**InkTransform**](inktransform-class.md) 物件。 **RotationTransform** 屬性會針對段落和繪圖元素傳回 **Null** 。

如需 **DivisionResult** 物件的詳細資訊，請參閱 [使用 DivisionResult 物件](working-with-the-divisionresult-object.md)。

 

 
