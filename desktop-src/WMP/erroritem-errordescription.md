---
title: ErrorItem. errorDescription
description: ErrorDescription 屬性會捕獲錯誤的描述。
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862788"
---
# <a name="erroritemerrordescription"></a>ErrorItem. errorDescription

**ErrorDescription** 屬性會捕獲錯誤的描述。

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

您應該設定 *設定*。如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *ErrorItem*。**errorDescription** 事件處理常式，以向使用者顯示錯誤訊息。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> </dl>

 

 





