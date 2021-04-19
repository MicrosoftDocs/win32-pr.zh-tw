---
description: Get \_ MaskName 方法會抓取要當做抹除遮罩使用的 JPEG 檔案名。
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'IDxtJpeg：： get_MaskName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977641"
---
# <a name="idxtjpegget_maskname-method"></a>IDxtJpeg：： get \_ MaskName 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`get_MaskName`方法會抓取要當做抹除遮罩使用之 JPEG 檔案的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[退出，retval\]
</dt> <dd>

接收檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果抹除轉換使用其支援的其中一個內建的 SMPTE 抹除，則此屬性的值為空字串。

呼叫端必須使用 **SysFreeString** 函數釋放傳回的字串。

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

[**IDxtJpeg 介面**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg：： get \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




