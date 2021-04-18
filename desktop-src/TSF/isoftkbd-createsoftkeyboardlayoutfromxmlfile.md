---
title: 'ISoftKbd CreateSoftKeyboardLayoutFromXMLFile 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeyboardLayoutFromXMLFile 方法會從指定的 XML 檔案建立軟鍵盤版面配置。
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- CreateSoftKeyboardLayoutFromXMLFile 方法文字服務架構
- CreateSoftKeyboardLayoutFromXMLFile 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardLayoutFromXMLFile 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968577"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>ISoftKbd：： CreateSoftKeyboardLayoutFromXMLFile 方法

**ISoftKbd：： CreateSoftKeyboardLayoutFromXMLFile** 方法會從指定的 XML 檔案建立軟鍵盤版面配置。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszKeyboardDesFile* \[在\]
</dt> <dd>

以零結尾的字串指標，表示 XML 檔案的名稱。

</dd> <dt>

*szFileStrLen* \[在\]
</dt> <dd>

以零結束的字串，指出 XML 檔案的長度。

</dd> <dt>

*pdwLayoutCookie* \[擴展\]
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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





