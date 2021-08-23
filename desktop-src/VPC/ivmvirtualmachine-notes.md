---
title: 'IVMVirtualMachine Notes 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器的附注。
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Notes 屬性虛擬電腦
- Notes 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine interface Virtual PC，Notes 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6e5e492330286bd60175983895a39ad7b0c91997f7fd36c966647d530a91c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471508"
---
# <a name="ivmvirtualmachinenotes-property"></a>IVMVirtualMachine：： Notes 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取和設定虛擬機器的附注。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a>屬性值

指定虛擬機器的附注。 字串的最大長度是65536個字元。

若要移除任何附注，請傳遞空字串。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                       |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                                          |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | 參數無效或包含超過65536個字元。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>                                       |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                   |



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

 

