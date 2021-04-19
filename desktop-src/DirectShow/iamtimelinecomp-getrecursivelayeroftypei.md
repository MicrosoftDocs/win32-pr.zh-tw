---
description: 不支援。 請改為呼叫 IAMTimelineComp：： GetRecursiveLayerOfType 方法。
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'IAMTimelineComp：： GetRecursiveLayerOfTypeI 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999178"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>IAMTimelineComp：： GetRecursiveLayerOfTypeI 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

不支援。 請改為呼叫 [**IAMTimelineComp：： GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppVirtualTrack* 
</dt> <dd>

保留的。

</dd> <dt>

*pWhichLayer* 
</dt> <dd>

保留的。

</dd> <dt>

*型別* 
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineComp 介面**](iamtimelinecomp.md)
</dt> </dl>

 

 




