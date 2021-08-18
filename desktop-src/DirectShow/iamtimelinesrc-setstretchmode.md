---
description: SetStretchMode 方法會設定延展模式。 如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'IAMTimelineSrc：： SetStretchMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c12d14edf665bb3257b627a194923c267ee9e8bd25027e40a7a975a15c10025f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148541"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>IAMTimelineSrc：： SetStretchMode 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetStretchMode`方法會設定延展模式。 如果影片的大小與輸出維度不符，則延展模式會決定影片來源的呈現方式。

## <a name="syntax"></a>語法


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nStretchMode* 
</dt> <dd>

指出目前延展模式的旗標。 如需可能值的清單，請參閱 [**調整旗標**](resize-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

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

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




