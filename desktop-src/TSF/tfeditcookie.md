---
title: 'TfEditCookie (Msctf) '
description: TfEditCookie 資料類型會識別具有鎖定的編輯會話。
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024548"
---
# <a name="tfeditcookie"></a>TfEditCookie

**TfEditCookie** 資料類型會識別具有鎖定的編輯會話。


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>備註

**TfEditCookie** 資料類型是由 TSF 管理員提供，而且用戶端 (應用程式或文字服務) 用來識別各種方法中具有唯讀或讀取/寫入鎖定的編輯會話。

**TfEditCookie** 值是以下列其中一種方式取得。

-   用戶端會呼叫 [ITfDocumentMgr：： CreateCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)。
-   TSF 管理員會呼叫用戶端 [ITfEditSession：:D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) 方法。
-   TSF 管理員會呼叫 client [ITfCompositionSink：： OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) 方法。
-   TSF 管理員會呼叫 client [ITfCleanupCoNtextSink：： OnCleanupCoNtext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) 方法。
-   TSF 管理員會呼叫 client [ITfTextEditSink：： OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                          |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITfCleanupCoNtextSink::OnCleanupCoNtext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr：： CreateCoNtext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession：:D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink::OnEndEdit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





