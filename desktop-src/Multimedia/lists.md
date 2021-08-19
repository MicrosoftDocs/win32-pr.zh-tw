---
title: 清單
description: 清單
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- 音訊 mixers，控制項
- 音訊 mixers，清單
- mixers，控制項
- mixers，清單
- 清單控制項
- MIXERCONTROLDETAILS_BOOLEAN 結構
- MIXERCONTROLDETAILS_LISTTEXT 結構
- 單一選取控制項
- 多重選取控制項
- 混音器控制項
- '多工器 (MUX) '
- 'MUX (多工器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f15e1c89e564ddd3b6c263b91242a3e4dc0382fd36f86554ec6bd0556191ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139393"
---
# <a name="lists"></a>清單

清單控制項提供複雜音訊線的單一選取或多重選取狀態。 這些控制項使用 [**MIXERCONTROLDETAILS 的 \_ 布林值**](/previous-versions//dd757295(v=vs.85)) 結構來取得和設定控制項屬性。 [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))結構也用來取得多重專案控制項的所有文字描述。 下表描述清單控制項的類型。



| 控制           | 描述                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 單一選取     | 一次將控制項選取範圍限制為一個專案。 與多工器控制項不同的是，此控制項可以用來控制音訊來源行以上的行。 例如，您可以使用此控制項，從混音器裝置所支援的篩選器清單中選取低傳遞篩選。 |
| 多工器 (MUX)  | 將一次行選取範圍限制為一個原始程式列。                                                                                                                                                                                                                       |
| 多重選取   | 可讓使用者同時選取清單中的多個專案。 不同于混音器控制項，多重選取控制項可以用來控制音訊來源行以上。                                                                                                  |
| Mixer             | 允許使用者同時從清單中選取來源行。                                                                                                                                                                                                               |



 

 

 