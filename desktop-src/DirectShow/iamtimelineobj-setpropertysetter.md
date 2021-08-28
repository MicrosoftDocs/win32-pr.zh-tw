---
description: SetPropertySetter 方法會設定物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。 在轉換和效果物件上呼叫這個方法。
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'IAMTimelineObj：： SetPropertySetter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c347296221cae30063a9d1e775252654df6b8daf592b2321b68d35067751ad15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213568"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a>IAMTimelineObj：： SetPropertySetter 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetPropertySetter`方法會設定物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。 在轉換和效果物件上呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* 
</dt> <dd>

屬性 setter [**IPropertySetter**](ipropertysetter.md) 介面的指標。

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

 

 




