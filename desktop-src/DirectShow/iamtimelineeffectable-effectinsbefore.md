---
description: EffectInsBefore 方法會將效果插入物件中指定的優先權層級。
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable：： EffectInsBefore 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0eca93a6c1837b8a7a8f5a95a6cdbf9e87f99191c0911a82e6fd7a3586eb8c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052748"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>IAMTimelineEffectable：： EffectInsBefore 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `EffectInsBefore` 效果插入物件中指定的優先權層級。

## <a name="syntax"></a>語法


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pfx* 
</dt> <dd>

效果的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。

</dd> <dt>

*優先順序* 
</dt> <dd>

要插入效果的優先權層級。 使用值-1，在優先順序清單的結尾插入效果。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK \_ ，如果物件不是有效的，則傳回 E >notimpl。 否則，會傳回另一個 **HRESULT** 值，指出錯誤的原因。

## <a name="remarks"></a>備註

必要時，效果的開始和停止時間會在物件的時間範圍界限內裁剪。 如果在指定的優先權層級已經有效果，該點的所有效果都會移至優先順序清單，以騰出空間給新的效果。

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

[**IAMTimelineEffectable 介面**](iamtimelineeffectable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




