---
title: 'TfGuidAtom (Msctf) '
description: TfGuidAtom 資料類型會識別 TSF 內的 GUID。 TfGuidAtom 是藉由呼叫 ITfCategoryMgr RegisterGUID 所取得。
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093776"
---
# <a name="tfguidatom"></a>TfGuidAtom

**TfGuidAtom** 資料類型會識別 TSF 內的 **GUID** 。 藉由呼叫 [**ITfCategoryMgr：： RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)，即可取得 **TfGuidAtom** 。


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a>備註

只有在呼叫 **ITfCategoryMgr：： RegisterGUID** 的進程內， **TfGuidAtom** 值才有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Msctf。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITfCategoryMgr：： GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[**ITfCategoryMgr::IsEqualTfGuidAtom**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





