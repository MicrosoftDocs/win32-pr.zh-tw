---
title: 'IVMAccountant CPUUtilizationHistory 屬性 (VPCCOMInterfaces .h) '
description: 將此虛擬機器的最新 CPU 使用率， (為百分比值陣列) 。
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- CPUUtilizationHistory 屬性 Virtual PC
- CPUUtilizationHistory 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，CPUUtilizationHistory 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466844"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a>IVMAccountant：： CPUUtilizationHistory 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將此虛擬機器的最新 CPU 使用率， (為百分比值陣列) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a>屬性值

此虛擬機器的最近 CPU 使用方式。 這項資料會以60個元素的陣列傳回，表示過去一分鐘內每秒的 CPU 使用率百分比。 Variant 類型是 VT \_ 陣列 \| vt \_ UI1。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                           |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                                              |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                    | 虛擬機器未執行。 所有60陣列元素都會設定為0。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

