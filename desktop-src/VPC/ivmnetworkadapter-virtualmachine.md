---
title: 'IVMNetworkAdapter VirtualMachine 屬性 (VPCCOMInterfaces .h) '
description: 抓取與此網路介面相關聯的虛擬機器。
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- VirtualMachine 屬性 Virtual PC
- VirtualMachine 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，VirtualMachine 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024535"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a>IVMNetworkAdapter：： VirtualMachine 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取與此網路介面相關聯的虛擬機器。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>屬性值

代表虛擬機器的 [**IVMVirtualMachine**](ivmvirtualmachine.md) 介面。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>        |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>           |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 找不到虛擬機器。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

