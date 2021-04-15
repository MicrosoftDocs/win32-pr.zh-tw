---
description: DivisionResult 物件代表分割物件所包含之筆觸的版面配置分析快照。 它包含來自版面配置分析的筆劃分類和群組資訊。
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: 使用 DivisionResult 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511920"
---
# <a name="working-with-the-divisionresult-object"></a>使用 DivisionResult 物件

**DivisionResult** 物件代表 **分割** 物件所包含之筆觸的版面配置分析快照。 它包含來自版面配置分析的筆劃分類和群組資訊。

您可以透過結構化元素類型（例如繪圖或手寫線）從 **DivisionResult** 物件取得資訊。 **DivisionResult** 物件可以在 **分割** 物件終結之後保存。 在自動化中，此物件稱為 [**IInkDivisionResult 介面**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件。

**DivisionResult** 物件的 [[**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)] 屬性包含在建立 **DivisionResult** 物件時，**分割** 物件中的 **筆劃** 集合副本。

[**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉會定義版面配置分析可辨識的結構化元素類型。

**DivisionResult** 物件的 [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype)方法會傳回 **DivisionUnits** 集合，其中包含指定型別的所有結構化元素。 個別的結構元素是由 **DivisionUnit** 物件表示。 每次呼叫 **ResultByType** 方法時， **DivisionResult** 物件都會建立 **DivisionUnits** 集合。 如需 **DivisionUnit** 物件的詳細資訊，請參閱 [使用 DivisionUnit 物件](working-with-the-divisionunit-object.md)。

 

 
