---
title: 標準 DISPID
description: 已針對控制項規格定義一些標準 dispid。
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af35ce4e4cad884b54bb0982037721608364a0249d3be6dd566f3aac766bb1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129780"
---
# <a name="standard-dispids"></a>標準 DISPID

已針對控制項規格定義一些標準 dispid。

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

整數類型的屬性。

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

Mousepointer 屬性可識別標準的滑鼠圖示。



| 值         | 描述                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  |  (由物件決定的預設) 圖形。<br/>                       |
| 1<br/>  | 箭號<br/>                                                           |
| 2<br/>  | 交叉 (交叉線指標) <br/>                                      |
| 3<br/>  | I 無線<br/>                                                          |
| 4<br/>  | 方塊內 (小方塊的圖示) <br/>                             |
| 5<br/>  | 大小 (四個指向北、南、東和西的箭號) <br/> |
| 6<br/>  | 大小 NE 的 SW (雙箭號指向東北和西南) <br/>      |
| 7<br/>  | 大小 N S (雙向箭號指向北和南) <br/>                |
| 8<br/>  | 大小 NW、SE<br/>                                                     |
| 9<br/>  | 大小 E W (雙向箭號指向東部和西部) <br/>                  |
| 10<br/> | 向上箭號<br/>                                                        |
| 11<br/> | 沙漏 (等候) <br/>                                                |
| 12<br/> | 不捨棄<br/>                                                         |
| 13<br/> | 箭號和沙漏<br/>                                             |
| 14<br/> | 箭號和問號<br/>                                         |
| 15<br/> | 全部大小<br/>                                                        |
| 99<br/> | MouseIcon 屬性指定的自訂圖示<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

圖片類型的屬性。

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>DISPID \_ 圖

圖片類型的屬性。

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ 有效

用來判斷控制項是否有有效的資料。

BOOL 類型的屬性。

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>DISPID 的 \_ 環境 \_ 調色板

用來允許控制項取得容器的 HPAL。 如果容器提供環境調色板，則這是可在前景中實現的唯一調色板。 想要實現本身調色板的控制項，在背景中必須這樣做。 如果容器未提供任何環境調色板，則現用控制項可以在前景中實現其調色板。 在 ActiveX SDK 的 OLE 控制項的調色板行為中，會進一步討論調色板的處理。

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





