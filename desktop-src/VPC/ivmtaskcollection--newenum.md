---
title: 'IVMTaskCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: '擷取集合的列舉值。 |IVMTaskCollection _NewEnum 屬性 (VPCCOMInterfaces) '
ms.assetid: 15c36bdb-5d26-4f67-aa7e-73b9bde2aa22
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMTaskCollection 介面
- IVMTaskCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMTaskCollection._NewEnum
- IVMTaskCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba76d1bf2bab1803521b66e150e049c871a4901f4ca64c739d7ed86542cb2b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752628"
---
# <a name="ivmtaskcollection_newenum-property"></a>IVMTaskCollection：： \_ NewEnum 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

擷取集合的列舉值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>屬性值

[IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉值。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>    |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 發生意外錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection 定義為5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMTaskCollection**](ivmtaskcollection.md)
</dt> </dl>

 

