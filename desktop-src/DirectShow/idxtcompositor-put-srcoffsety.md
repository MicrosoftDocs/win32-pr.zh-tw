---
description: Put \_ SrcOffsetY 方法會指定來源矩形的垂直位移。
ms.assetid: abdc520f-8de6-4a4f-aa8f-facedaa8fce1
title: 'IDxtCompositor：:p ut_SrcOffsetY 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e12a6b253b1b8704092dcb9c776120917104277b52e1c6fe815bf365ba7dd691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651248"
---
# <a name="idxtcompositorput_srcoffsety-method"></a>IDxtCompositor：:p 的 \_ SrcOffsetY 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_SrcOffsetY`方法會指定來源矩形的垂直位移。

## <a name="syntax"></a>語法


```C++
HRESULT put_SrcOffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

來源矩形的垂直位移（以圖元為單位）。

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

[**IDxtCompositor 介面**](idxtcompositor.md)
</dt> </dl>

 

 




