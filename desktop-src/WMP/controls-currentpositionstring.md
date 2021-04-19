---
title: CurrentPositionString
description: CurrentPositionString 屬性會將媒體專案中的目前位置抓取為格式化為 HH MM SS (小時、分鐘和秒) 的字串。
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- CurrentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979540"
---
# <a name="controlscurrentpositionstring"></a>CurrentPositionString

**CurrentPositionString** 屬性會將媒體專案中的目前位置抓取為格式化為 HH： MM： SS (小時、分鐘和秒) 的 **字串**。

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

如果媒體專案的長度不到一小時，則不會包含 HH：部分。

> [!Note]  
> 當媒體專案停止或暫停時，您應該包含程式碼以停止計時器。

 

## <a name="examples"></a>範例

下列 JScript 範例會啟動 HTML 計時器，以一秒的間隔顯示媒體檔案的目前位置。 已建立名為 MyText 的 HTML 文字元素，以顯示目前的位置。 使用 ID = "Player" 建立 **player** 物件。


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> </dl>

 

 





