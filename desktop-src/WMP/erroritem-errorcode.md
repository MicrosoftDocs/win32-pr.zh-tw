---
title: ErrorItem。 errorCode
description: ErrorCode 屬性會捕獲目前的錯誤碼。
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem，errorCode Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f426bbaf1092b64cdb3578cb681282c9b27d9d2e2e23a69d50f9c065353ad104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577702"
---
# <a name="erroritemerrorcode"></a>ErrorItem。 errorCode

**ErrorCode** 屬性會捕獲目前的錯誤碼。

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

您應該設定 *設定*。如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *ErrorItem*。事件處理常式中的 **errorCode** ，可向使用者顯示錯誤碼。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





