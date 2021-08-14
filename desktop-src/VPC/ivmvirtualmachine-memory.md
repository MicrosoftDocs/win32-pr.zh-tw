---
title: 'IVMVirtualMachine Memory 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中的實體記憶體數量（以 mb 為單位）。
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Memory 屬性 Virtual PC
- Memory 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Memory 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a828dde1804e546c97fe7cd2c161fc45366d416ba0e44900816c7bbee4b1ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344662"
---
# <a name="ivmvirtualmachinememory-property"></a>IVMVirtualMachine：： Memory 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取和設定虛擬機器中的實體記憶體數量（以 mb 為單位）。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>屬性值

指定實體記憶體的數量（以 mb 為單位）。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                         | 意義                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>                  |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>              | 參數為 **Null**。<br/>                     |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | 參數無效或超出範圍。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>      | 未知的設定。<br/>                  |
| <dl> <dt>VM \_E \_ PREF \_ \_ 找不到</dt> <dt>0xA0040300</dt> </dl> | 找不到喜好設定。<br/>                  |
| <dl> <dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | 虛擬機器正在執行或已儲存。<br/>       |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/>              |



## <a name="remarks"></a>備註

虛擬機器中的實體記憶體數量必須至少為 4 MB。 記憶體的上限取決於主機設定，但最多可以是 3712 MB。

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

 

