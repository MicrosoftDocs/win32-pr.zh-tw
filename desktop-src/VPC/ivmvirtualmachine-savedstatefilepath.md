---
title: 'IVMVirtualMachine SavedStateFilePath 屬性 (VPCCOMInterfaces .h) '
description: 抓取儲存狀態檔案的完整路徑。
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- SavedStateFilePath 屬性 Virtual PC
- SavedStateFilePath 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SavedStateFilePath 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97bbb55ed4a784dad897fad480a2d9175db2759bba754308dc9b845f7190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752230"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a>IVMVirtualMachine：： SavedStateFilePath 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取儲存狀態檔案的完整路徑。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a>屬性值

虛擬機器儲存狀態檔案的完整路徑。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                              | 意義                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                 | 作業成功。<br/>                           |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                   | 參數為 **Null**。<br/>                              |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>           | 未知的設定。<br/>                           |
| <dl> <dt>VM \_E \_ VM \_ 沒有 \_ 儲存的 \_ 狀態</dt> <dt>0xA00400501</dt> </dl> | 虛擬機器沒有相關聯的儲存狀態檔案。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>           | 已發生未預期的錯誤。<br/>                       |



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

 

