---
title: Error。 item 方法
description: Item 方法會從錯誤佇列中取出 ErrorItem 物件。
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，Error 類別
- Error 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339693"
---
# <a name="erroritem-method"></a>Error。 item 方法

**Item** 方法會從錯誤佇列中取出 **ErrorItem** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**Long**) ，其中包含要抓取之 **ErrorItem** 物件的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **ErrorItem** 物件。

## <a name="remarks"></a>備註

Windows Media Player 可能會產生一些錯誤，以回應錯誤狀況。 這個方法可讓您使用索引編號來抓取佇列中的特定錯誤。 錯誤佇列的索引編號開頭為零。

您應該設定 *設定*。如果您選擇顯示自訂錯誤訊息，請 **enableErrorDialogs** 為 false。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *錯誤*。事件處理常式中的 **專案** 物件，警示使用者最新的錯誤。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

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
</dt> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> </dl>

 

 





