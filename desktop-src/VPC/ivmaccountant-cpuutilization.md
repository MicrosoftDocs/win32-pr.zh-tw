---
title: 'IVMAccountant CPUUtilization 屬性 (VPCCOMInterfaces .h) '
description: 抓取此虛擬機器目前的 CPU 使用率百分比。
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization 屬性 Virtual PC
- CPUUtilization 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，CPUUtilization 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba54d7ec3a3fc447a49e9a72addd72fc5e3929b486c8fd4271276a40a7041f4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007304"
---
# <a name="ivmaccountantcpuutilization-property"></a>IVMAccountant：： CPUUtilization 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此虛擬機器目前的 CPU 使用率百分比。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>屬性值

目前的 CPU 使用率百分比。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>       |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>          |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                    | 虛擬機器未執行。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

