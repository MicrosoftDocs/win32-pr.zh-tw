---
title: 'ISoftKbd GetSoftKeyboardTextFont 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardTextFont 方法會抓取軟鍵盤所使用的文字字型。
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- GetSoftKeyboardTextFont 方法文字服務架構
- GetSoftKeyboardTextFont 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardTextFont 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105251"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>ISoftKbd：： GetSoftKeyboardTextFont 方法

**ISoftKbd：： GetSoftKeyboardTextFont** 方法會抓取軟鍵盤所使用的文字字型。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLogFont* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中取得 [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構，以定義軟鍵盤的文字字型。

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

