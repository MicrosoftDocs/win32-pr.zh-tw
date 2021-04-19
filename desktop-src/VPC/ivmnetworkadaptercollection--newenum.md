---
title: 'IVMNetworkAdapterCollection _NewEnum 屬性 (VPCCOMInterfaces) '
description: '擷取集合的列舉值。 |IVMNetworkAdapterCollection _NewEnum 屬性 (VPCCOMInterfaces) '
ms.assetid: 9b970fc6-f8a3-4a16-9d59-789a59a99b68
keywords:
- _NewEnum 屬性 Virtual PC
- _NewEnum 屬性 Virtual PC，IVMNetworkAdapterCollection 介面
- IVMNetworkAdapterCollection 介面 Virtual PC，_NewEnum 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection._NewEnum
- IVMNetworkAdapterCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf118700a81865ff93ee581cbb2efd07d237805
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998977"
---
# <a name="ivmnetworkadaptercollection_newenum-property"></a>IVMNetworkAdapterCollection：： \_ NewEnum 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

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
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                           |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

