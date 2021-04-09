---
title: 'IVMVirtualMachine 會計屬性 (VPCCOMInterfaces .h) '
description: 捕獲此虛擬機器的會計。
ms.assetid: 5e512b83-8630-46ee-b521-c8a8193727f5
keywords:
- 會計內容虛擬電腦
- 會計內容虛擬 PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，會計師屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Accountant
- IVMVirtualMachine.get_Accountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af1212de041b1d4c5bda59b9b12ab1d715be67cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106044"
---
# <a name="ivmvirtualmachineaccountant-property"></a>IVMVirtualMachine：：會計師屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捕獲此虛擬機器的會計。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Accountant(
  [out, retval] IVMAccountant **accountant
);
```



## <a name="property-value"></a>屬性值

[**IVMAccountant**](ivmaccountant.md)物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>     |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

