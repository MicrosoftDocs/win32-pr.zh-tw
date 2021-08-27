---
title: 排程的工作專案
description: 工作排程器會使用兩個詞彙來描述其可以排程工作專案和工作的內容。
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- 工作專案工作排程器
- 工作專案工作排程器，相較于工作
- 工作工作排程器
- 工作工作排程器，相較于工作專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080428"
---
# <a name="scheduled-work-items"></a>排程的工作專案

工作排程器會使用兩個詞彙來描述它可以排程的內容：工作專案和工作。 在這兩個詞彙中， [*工作專案*](w.md) 是更一般的詞彙，描述可排程的任何專案類型。 *工作專案* 可以是工作排程器服務在專案觸發程式 () 所指定的時間執行的任何專案。

相反地，工作 [*是特定*](t.md) 類型的工作專案。 目前唯一支援的排程工作專案類型是工作。

[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面包含所有類型的已排程工作專案所支援的方法。 例如，帳戶資訊、執行時間和應用程式定義的批註都是可套用至所有工作專案類型的屬性。 這些屬性可以透過 **IScheduledWorkItem** 介面設定和抓取。

[**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面只包含工作所支援的方法。

[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面的方法目前是由 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所繼承，未來將會由其他工作專案介面繼承。

| 範例                                              | 請參閱                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| 建立新的工作。                                         | [使用 NewWorkItem 範例建立工作](creating-a-task-using-newworkitem-example.md) |
| 正在執行現有的工作。                                    | [啟動工作範例](starting-a-task-example.md)                                     |
| 正在抓取適用于所有工作專案類型的屬性。 | [正在抓取工作專案屬性範例](retrieving-work-item-property-examples.md)       |
| 設定適用于所有工作專案類型的屬性。    | [設定工作專案屬性範例](setting-work-item-property-examples.md)             |



 

 

 




