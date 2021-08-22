---
description: Microsoft 辨識器會使用下列 Guid。
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: 屬性 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4883ee713122ae36c4ad7e29b86013beb670545ffac31da28bad4da8c2f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031656"
---
# <a name="property-guids"></a>屬性 Guid

Microsoft 辨識器會使用下列 Guid。 如果可能的話，應用程式應該使用這些 Guid。 不過，在預期的情況下，其他辨識器會針對不受 Microsoft 辨識器支援的屬性使用額外的 Guid。

已開發所有屬性函式，並瞭解 Guid 清單可能會由其他辨識器延伸。 這些屬性函數包括：

-   [**GetCoNtextPropertyList 函式**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetCoNtextPropertyValue 函式**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList 函式**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetCoNtextPropertyValue 函式**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

下表列出在 msinkaut 中所定義的 Tablet PC 屬性 Guid (安裝于 c： \\ Program Files \\ MICROSOFT Tablet PC Platform SDK \\ 預設) 。



| GUID                                                  | 定義                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Box 模式中的辨識器替代方塊索引<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | 行號<br/>                                                                   |
| INKRECOGNITIONPROPERTY \_ 分割<br/>       | 辨識器如何分割單字和字元<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | 手勢作用點<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | 區段的最大筆觸數目<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | 每英寸點數計量<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**信賴度 \_層級**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) 列舉<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | >Lattice 中使用的計算基準、中線或兩者的相關資訊<br/> |



 

 

 




