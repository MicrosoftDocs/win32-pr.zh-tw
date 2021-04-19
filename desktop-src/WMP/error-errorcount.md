---
title: 錯誤。 errorCount
description: ErrorCount 屬性會捕獲錯誤佇列中的錯誤數目。
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- 錯誤。 errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985959"
---
# <a name="errorerrorcount"></a>錯誤。 errorCount

**ErrorCount** 屬性會捕獲錯誤佇列中的錯誤數目。

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。

## <a name="examples"></a>範例

下列 JScript 範例使用 *錯誤*。在事件處理常式中 **errorCount** ，以警示使用者錯誤佇列中的最新錯誤。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Error 物件**](error-object.md)
</dt> </dl>

 

 





