---
title: 'TfClientId (Msctf) '
description: TfClientId 資料類型是用來識別用戶端。
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685751"
---
# <a name="tfclientid"></a>TfClientId

**TfClientId** 資料類型是用來識別用戶端。


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>備註

在 TSF 中，應用程式和文字服務通常稱為用戶端。 每個用戶端都會收到唯一的識別碼，以在呼叫各種 TSF manager 方法時用來識別其本身。 此識別碼屬於 **TfClientId** 類型。

**TfClientId** 資料類型是由 TSF 管理員所提供。 應用程式會在呼叫 [ITfThreadMgr：： Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)時取得 **TfClientId** 值。 文字服務的 TfClientId 值會傳遞至 [ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) 方法。 任何不符合上述類別的物件都可以藉由呼叫 [ITfClientId：： GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)來取得用戶端識別碼。

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

[**ITfClientId::GetClientId**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor：： Activate**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr：： Activate**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





