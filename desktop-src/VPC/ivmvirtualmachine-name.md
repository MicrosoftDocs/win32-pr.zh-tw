---
title: 'IVMVirtualMachine Name 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器設定的名稱。
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104100"
---
# <a name="ivmvirtualmachinename-property"></a>IVMVirtualMachine：： Name 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取和設定虛擬機器設定的名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>屬性值

指定虛擬機器設定的名稱。 名稱的長度不能超過80個字元，且包含虛擬機器名稱設定檔的完整路徑總長度不能超過 **最大 \_ 路徑** (260) 個字元。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                    | 意義                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                       | 作業成功。<br/>                                                        |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                         | 參數為 **Null**。<br/>                                                           |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | 參數無效或為空字串。<br/>                                    |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>                 | 未知的設定。<br/>                                                        |
| <dl> <dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl>            | 虛擬機器正在執行或已儲存。<br/>                                             |
| <dl> <dt>VM \_E \_ 設定 \_ 沒有 \_ 名稱</dt> <dt>0xA0040400</dt> </dl>            | *VirtualMachineName* 參數是空的。<br/>                                         |
| <dl> <dt>VM \_E \_ CONFIG \_ NAME \_ 太 \_ 長</dt> <dt>0xA00400401</dt> </dl>    | 參數包含太多字元。<br/>                                          |
| <dl> <dt>VM \_E \_ CONFIG \_ NAME \_ 不正確 \_ CHAR</dt> <dt>0xA0040402</dt> </dl> | 參數包含下列其中一個無效字元 " \* ？： <>/ \| \\ " "。<br/> |
| <dl> <dt>VM \_E \_ 設定 \_ 重複 \_ 名稱</dt> <dt>0xA0040403</dt> </dl>     | 指定的名稱已存在，作為另一部虛擬機器的名稱。<br/>            |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                 | 已發生未預期的錯誤。<br/>                                                    |



## <a name="remarks"></a>備註

虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。 這是 [**IVMVirtualMachine**](ivmvirtualmachine.md)的預設屬性。

如果 VPC.exe 正在執行，且 VM 已儲存，則設定 [ **名稱** ] 屬性將會失敗。 如果 VPC.exe 未執行且儲存了 VM，則下次啟動 VPC.exe 時，設定 **Name** 屬性會成功。

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

 

