---
title: 'IVMVirtualMachine UndoAction 屬性 (VPCCOMInterfaces .h) '
description: 當 VM 關閉時，要在所有復原磁片磁碟機上執行的預設動作。
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction 屬性 Virtual PC
- UndoAction 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，UndoAction 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466377"
---
# <a name="ivmvirtualmachineundoaction-property"></a>IVMVirtualMachine：： UndoAction 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

當虛擬機器 (VM) 使用 [**TurnOff**](ivmvirtualmachine-turnoff.md) 方法關閉，或使用 [**關閉**](ivmguestos-shutdown.md) 方法關閉，或從客體作業系統中關閉時，會抓取並設定要在所有復原磁片磁碟機上執行的預設動作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a>屬性值

指定當 VM 從客體作業系統中關閉時，要在所有復原磁片磁碟機上執行的預設動作。 如需值的清單，請參閱 [**VMUndoAction**](vmundoaction.md)。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | 參數無效。<br/>       |
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

 

