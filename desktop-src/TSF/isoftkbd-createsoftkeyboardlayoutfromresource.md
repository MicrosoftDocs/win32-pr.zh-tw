---
title: 'ISoftKbd CreateSoftKeyboardLayoutFromResource 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeybboardLayoutFromResource 方法會從指定的資源建立軟鍵盤版面配置。
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- CreateSoftKeyboardLayoutFromResource 方法文字服務架構
- CreateSoftKeyboardLayoutFromResource 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardLayoutFromResource 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969992"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>ISoftKbd：： CreateSoftKeyboardLayoutFromResource 方法

**ISoftKbd：： CreateSoftKeybboardLayoutFromResource** 方法會從指定的資源建立軟鍵盤版面配置。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszResFile* \[在\]
</dt> <dd>

以零結尾的字串指標，指出資源檔的名稱。

</dd> <dt>

*lpszResType* \[在\]
</dt> <dd>

表示資源類型之以零結尾的字串指標。

</dd> <dt>

*lpszXMLResString* \[在\]
</dt> <dd>

識別資源之以零結尾的字串指標。

</dd> <dt>

*lpdwLayoutCookie* \[擴展\]
</dt> <dd>

緩衝區的指標，此方法會在其中捕獲軟鍵盤配置 cookie。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/> |



 

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

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





