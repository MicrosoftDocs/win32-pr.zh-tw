---
description: IAMTimelineObj：： GetDirtyRange2 方法-不支援。
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'IAMTimelineObj：： GetDirtyRange2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119516"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a>IAMTimelineObj：： GetDirtyRange2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

不支援。

## <a name="syntax"></a>語法


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

保留的。

</dd> <dt>

*pStop* 
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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> </dl>

 

 




