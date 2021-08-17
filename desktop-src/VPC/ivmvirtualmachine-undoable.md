---
title: IVMVirtualMachine (VPCCOMInterfaces) 的能撤銷屬性
description: 判斷是否已針對連接至 VM 的硬碟啟用復原磁片磁碟機。
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- 虛擬 PC 的能撤銷
- 虛擬 PC、IVMVirtualMachine 介面、虛擬機器
- IVMVirtualMachine 介面虛擬 PC、能撤銷的屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7663cefb8f94809f0fd016e002102c9956066b64ca21fb79766598b592ec3dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752071"
---
# <a name="ivmvirtualmachineundoable-property"></a>IVMVirtualMachine：：無法撤銷的屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷是否已針對連接到虛擬機器 (VM) 的硬碟啟用復原磁片磁碟機。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a>屬性值

如果已針對連接至 VM 的硬碟啟用復原磁片磁碟機， **則指定 variant \_ TRUE** ，否則為 **variant \_** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                         | 意義                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>     |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>              | 參數為 **Null**。<br/>        |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>      | 未知的設定。<br/>     |
| <dl> <dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | VM 正在執行或已儲存。<br/>       |



## <a name="remarks"></a>備註

如果停用復原磁片磁碟機，將會刪除任何現有的復原磁片磁碟機檔案。

如果 VM 正在執行或已儲存，您就無法設定此屬性。

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

 

