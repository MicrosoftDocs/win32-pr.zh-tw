---
title: 'ISoftKbd SetSoftKeyboardTextFont 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardTextFont 方法會設定軟鍵盤所使用的文字字型。
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- SetSoftKeyboardTextFont 方法文字服務架構
- SetSoftKeyboardTextFont 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardTextFont 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965924"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>ISoftKbd：： SetSoftKeyboardTextFont 方法

**ISoftKbd：： SetSoftKeyboardTextFont** 方法會設定軟鍵盤所使用的文字字型。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLogFont* \[在\]
</dt> <dd>

[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構定義了軟鍵盤的文字字型。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PLogFont* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

