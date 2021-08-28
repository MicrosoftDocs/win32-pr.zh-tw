---
description: SetMuted 方法會設定物件的已靜音狀態。 靜音物件不會呈現，但會保留在時間軸中。
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj：： SetMuted 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c561dad9435d972b24a899a9dd7aa65207555b3373fc2930438328aa17568fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633878"
---
# <a name="iamtimelineobjsetmuted-method"></a>IAMTimelineObj：： SetMuted 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetMuted`方法會設定物件的已靜音狀態。 靜音物件不會呈現，但會保留在時間軸中。

## <a name="syntax"></a>語法


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* 
</dt> <dd>

指定靜音狀態的旗標。 若 **為 TRUE**，表示物件及其所有子系都已靜音。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

將物件靜音，也會靜音物件中包含的任何子系。 例如，如果您將曲目靜音，該播放軌的轉換、來源和效果也會靜音。 一旦物件不再為靜音，其子系會還原為其先前的狀態，可能是靜音或 unmuted。

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

 

 




