---
title: ClearErrorQueue 方法
description: ClearErrorQueue 方法會清除錯誤佇列中的錯誤。 |ClearErrorQueue 方法
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- clearErrorQueue 方法 Windows Media Player
- clearErrorQueue 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，clearErrorQueue 方法
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999208"
---
# <a name="errorclearerrorqueue-method"></a>ClearErrorQueue 方法

**ClearErrorQueue** 方法會清除錯誤佇列中的錯誤。

## <a name="syntax"></a>語法


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在處理一系列的錯誤之後，這個方法會很有用來清除錯誤佇列。

您 *應該設定設定。* 如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。

## <a name="examples"></a>範例

下列 JScript 範例使用 *錯誤*。**clearErrorQueue** 事件處理常式，在顯示所有錯誤描述之後清空錯誤佇列。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

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

 

 





