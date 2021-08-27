---
description: Get BorderWidth 方法會抓取抹除 \_ 模式邊緣的實心框線寬度。
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'IDxtJpeg：： get_BorderWidth 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32f2632c62cadd717232e2febc9ed7e834b7ea11c38fa49522e05b2383cb845d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131058"
---
# <a name="idxtjpegget_borderwidth-method"></a>IDxtJpeg：： get \_ BorderWidth 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會在抹除 `get_BorderWidth` 模式的邊緣上抓取實線框線的寬度。

## <a name="syntax"></a>語法


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收框線的寬度（以圖元為單位）。

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

[**IDxtJpeg 介面**](idxtjpeg.md)
</dt> </dl>

 

 




