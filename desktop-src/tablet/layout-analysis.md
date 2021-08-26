---
description: 版面配置分析是在筆劃集合上操作，並且將筆劃分類為手寫和繪圖元素。 分隔物件提供對 Tablet PC 版面配置分析功能的存取。
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: 版面配置分析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8131859dd7e4c7bd6927db42bd605541001ac0f1222bfbf27b0e59809d4b7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934818"
---
# <a name="layout-analysis"></a>版面配置分析

版面配置分析是在 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合上操作，並且將筆劃分類為手寫和繪圖元素。 [**分隔**](inkdivider-class.md)物件提供對 Tablet PC 版面配置分析功能的存取。

下表描述 [**分隔**](inkdivider-class.md)物件將筆劃分類至 [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype)列舉的結構化元素類型。



| 類型          | 描述                                                                      |
|---------------|----------------------------------------------------------------------------------|
| **區段**   | 辨識區段。<br/>                                                |
| **線條**      | 包含一或多個辨識區段的手寫行。<br/> |
| **Paragraph** | 包含一或多行手寫的筆劃區塊。<br/>    |
| **繪圖**   | 非手寫的筆墨。<br/>                                          |



 

[**分割**](inkdivider-class.md)物件具有 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，其 **會在您** 每次在集合中加入或刪除時動態分析。 **分割** 物件不可序列化，而且您無法儲存其分析狀態。 因此， **分隔** 物件是針對必須區分混合手寫和繪圖輸入的應用程式所設計，但不需要重新分析會話之間的大量筆跡。

您可以取得目前分析結果的靜態快照集，這會在 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件中傳回。 您可以取得 [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) 物件，每個物件都代表 **DivisionResult** 物件的單一結構元素。 **DivisionResult** 和 **DivisionUnit** 物件不是可序列化的。 不過，這些物件的狀態資訊可供使用。

[**分隔**](inkdivider-class.md)物件僅適用于由左至右書寫。 若要讓 **分隔** 物件能夠正確地分析垂直語言（例如中文），必須從左至右（而不是從上到下）繪製字元。

 

