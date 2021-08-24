---
description: 要求應用程式暫停操作延遲。
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'ISuspendingOperation：： GetDeferral 方法 (Windows。ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 4a64ed4449c2e11ebeec9194adb7fd69ecc7227efa9df36a6900f4139e44ec4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794988"
---
# <a name="isuspendingoperationgetdeferral-method"></a>ISuspendingOperation：： GetDeferral 方法

要求應用程式暫停操作延遲。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*延遲* \[退出，retval\]
</dt> <dd>

延遲暫停。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 標頭<br/>                   | <dl> <dt>Windows。ApplicationModel。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows。ApplicationModel .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




