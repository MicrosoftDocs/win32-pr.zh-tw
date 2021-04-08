---
description: 在網路監視器中，capture 篩選器是由 CAPTUREFILTER 結構所定義。
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: CAPTUREFILTER 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943507"
---
# <a name="the-capturefilter-structure"></a>CAPTUREFILTER 結構

在網路監視器中， [capture 篩選器](capture-filters.md) 是由 [**CAPTUREFILTER**](capturefilter.md) 結構所定義。 旗標、值和運算式的遺漏或組合，會決定網路監視器驅動程式會將哪些框架傳遞或卸載。 下圖顯示「capture 濾波器分析」的三個區域： Etype/SAP、address 和 pattern match。

![capture 篩選器分析的三個區域](images/capfilter.png)

下表列出每個 capture 篩選元素的函式。



| Filter 元素                                       | 動作                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etype/SAP](writing-etypesap-filter-portion.md)     | 評估 Etype/SAP 設定。 旗標的組合可決定要包含或排除的設定類型或值。                                                                                    |
| [位址](writing-addresstable-filter-portion.md)   | 評估來源和目的地位址和位址組。 不同的旗標組合可決定要包含或排除的個別值或位址組組合。                   |
| [模式比對](writing-the-patternmatch-filter.md) | 定義框架內的複雜模式比對。 針對不同的類型和位移提供旗標。 您可以結合模式比對與邏輯 AND 或 or 運算子語句。                              |
| [裁剪](clipping-a-frame.md)                     | 以各種位元組值所指定的方式來剪輯框架。 您只能使用這個專案來裁剪所有框架，或將它與其他 capture 濾波器元素搭配使用;例如，若要尋找並裁剪單一畫面格。 |
| [**觸發**](trigger.md)                           | 此 capture 篩選元素已淘汰。 觸發程式已不再是 capture 篩選準則的一部分;它們現在包含在自己的 BLOB 標籤中，這些標記是個別指定的。                                     |



 

畫面格會針對 capture 篩選器的所有三個部分進行評估。 因此，成功傳輸的框架必須通過每個元素。 請注意，網路監視器驅動程式會將上述三個元素中的任何專案都評估為 **TRUE**。 例如，驅動程式會將不存在的 Etype/SAP 區段評估為「所有具有任何 Etype/SAP 值的框架都有效」。

 

 



