---
title: 'IVMVirtualPC UnregisterVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 取消註冊 VM 設定，而不刪除設定檔。
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine 方法 Virtual PC
- UnregisterVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，UnregisterVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6173d6f43d51384af610b850ec654d185f0a8ce31a375b4dd90bd929c6455b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652728"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a>IVMVirtualPC：： UnregisterVirtualMachine 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

在不刪除設定檔的情況下，取消註冊 (VM) 設定的虛擬機器。

## <a name="syntax"></a>語法


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*virtualMachine* \[在\]
</dt> <dd>

[**IVMVirtualMachine**](ivmvirtualmachine.md)物件的指標，代表要取消註冊的 VM 設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                        | 描述                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                | *VirtualMachine* 參數為 **Null**。<br/>                                         |
| <dl> <dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt> </dl>                        | VM 正在執行。<br/>                                                                   |
| <dl> <dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt> </dl> | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                        | 已發生未預期的錯誤。<br/>                                                    |



 

## <a name="remarks"></a>備註

只有已停止的 Vm 可以取消註冊。 當 VM 取消註冊時，此設定的現有儲存狀態或復原磁片磁碟機資料將會保留。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

