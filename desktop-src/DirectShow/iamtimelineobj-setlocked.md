---
description: SetLocked 方法會將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'IAMTimelineObj：： SetLocked 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 87298b4e1fe9bc821c72d46d09d55e898b453292940029b7189a92e455b4c206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052478"
---
# <a name="iamtimelineobjsetlocked-method"></a>IAMTimelineObj：： SetLocked 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetLocked`方法會將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。

鎖定狀態表示不應編輯物件;解除鎖定狀態表示可以編輯物件。 時間軸不會強制執行鎖定。 鎖定的設定只存在於應用程式的便利性。

## <a name="syntax"></a>語法


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* 
</dt> <dd>

指定物件之編輯狀態的布林值。 若 **為 TRUE**，則物件已鎖定，不應該編輯。 如果 **為 FALSE**，則表示物件已解除鎖定，而且可以進行編輯。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




