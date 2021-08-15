---
title: 'ISoftKbd SetSoftKeyboardColors 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardColors 方法會為指定的色彩類型設定軟鍵盤色彩。
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- SetSoftKeyboardColors 方法文字服務架構
- SetSoftKeyboardColors 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardColors 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877369"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>ISoftKbd：： SetSoftKeyboardColors 方法

**ISoftKbd：： SetSoftKeyboardColors** 方法會為指定的色彩類型設定軟鍵盤色彩。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*colorType* \[在\]
</dt> <dd>

值，指定軟鍵盤的色彩類型。 可能的值是針對 [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) 列舉而定義的。

</dd> <dt>

*色彩* \[在\]
</dt> <dd>

指定 RGB 色彩的32位 [**COLORREF**](/windows/desktop/gdi/colorref) 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 其中一個參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

