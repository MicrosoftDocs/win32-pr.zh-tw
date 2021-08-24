---
title: 'IVMVirtualMachine Startup2 方法 (VPCCOMInterfaces .h) '
description: 使用 advanced 選項，從未初始化或已儲存的狀態啟動虛擬機器。
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Startup2 方法 Virtual PC
- Startup2 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Startup2 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b76364f80d9faaaeeb0f9760ce434d91658afc6699a7acdeee98f0a2e65548d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652888"
---
# <a name="ivmvirtualmachinestartup2-method"></a>IVMVirtualMachine：： Startup2 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

使用 advanced options 從未初始化或已儲存的狀態啟動虛擬機器 (VM) 。

即使父磁片的時間戳記已變更，此方法也會提供一種機制來啟動具有差異磁片的 VM。

## <a name="syntax"></a>語法


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*startupOption* \[在\]
</dt> <dd>

Advanced 啟動選項。 可能的值來自 [**VMStartupOption**](vmstartupoption.md) 列舉。

</dd> <dt>

*startupTask* \[退出，retval\]
</dt> <dd>

[**IVMTask**](ivmtask.md)物件，用來追蹤開始順序的完成進度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | 描述                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                | 作業成功。<br/>                                     |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | *StartupOption* 參數無效。<br/>                       |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                  | *StartupTask* 參數為 **Null**。<br/>                          |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 呼叫端必須具有執行存取權限，才能啟動此 VM。<br/> |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                           | 作業未及時完成。<br/>                |
| <dl> <dt>**VM \_E \_ 0xA0040203 \_ \_ 資源**</dt> <dt></dt> </dl>                    | 沒有足夠的主機資源。<br/>                              |
| <dl> <dt>**VM \_電子 \_ 0xA0040204 太 \_ 多 \_ vm**</dt> <dt></dt> </dl>                       | 有太多作用中的 Vm。<br/>                                    |
| <dl> <dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt> </dl>                          | VM 已在執行中。<br/>                                        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                          | 已發生未預期的錯誤。<br/>                                 |



 

## <a name="remarks"></a>備註

下列值可透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性來傳回。



| [**錯誤碼**](ivmtask-error.md) /值                                                                                                                                                                                                                                      | 描述                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950) <br/>                                                 | 硬體不支援虛擬化。<br/>              |
| <span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951) <br/> | 硬體虛擬化已停用。<br/>                       |
| <span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952) <br/>                             | virtual pc 2007 和 Windows virtual pc 皆已安裝。<br/> |
| <span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953) <br/>             | 已安裝其他虛擬化軟體。<br/>                |
| <span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203) <br/>                                                                 | 沒有足夠的主機資源。<br/>                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

