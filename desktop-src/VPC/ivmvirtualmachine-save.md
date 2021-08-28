---
title: 'IVMVirtualMachine Save 方法 (VPCCOMInterfaces .h) '
description: 將虛擬機器 (VM) 狀態。
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- 儲存方法 Virtual PC
- 儲存方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Save 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609125ed9ae8deab897163d6a841e9cb665659c2c5af76baff3a1d96fb235e92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124788"
---
# <a name="ivmvirtualmachinesave-method"></a>IVMVirtualMachine：： Save 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將虛擬機器 (VM) 狀態。

## <a name="syntax"></a>語法


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*saveTask* \[退出，retval\]
</dt> <dd>

[**IVMTask**](ivmtask.md)物件，可用來追蹤 VM 狀態儲存順序的完成進度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | 描述                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                | 作業成功。<br/>                                                 |
| <dl> <dt>**E \_FAIL**</dt> <dt>0x80004005</dt> </dl>                                     | 因為復原磁片已標示為要刪除，所以無法儲存 VM。<br/>    |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                  | 參數為 **Null**。<br/>                                                    |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 呼叫端必須具有執行存取權限，才能儲存此 VM 的狀態。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                     | VM 未執行。<br/>                                                        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                          | 已發生未預期的錯誤。<br/>                                             |



 

## <a name="remarks"></a>備註

當 **儲存** 工作達到完成時，VM 會關閉。 [**IVMVirtualMachine：： State**](ivmvirtualmachine-state.md)屬性會在儲存進行中時包含 **vmVMState \_ 儲存**，接著在儲存完成並關閉 VM 時 **\_ 儲存 vmVMState** 。

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

 

