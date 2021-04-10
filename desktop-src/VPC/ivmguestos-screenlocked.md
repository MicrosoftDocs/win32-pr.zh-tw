---
title: 'IVMGuestOS ScreenLocked 屬性 (VPCCOMInterfaces .h) '
description: 指出是否已鎖定客體作業系統中的畫面。
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- ScreenLocked 屬性 Virtual PC
- ScreenLocked 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，ScreenLocked 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025196"
---
# <a name="ivmguestosscreenlocked-property"></a>IVMGuestOS：： ScreenLocked 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指出是否已鎖定客體作業系統中的畫面。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a>屬性值

**變異 \_** 如果在客體作業系統中鎖定螢幕，則為 TRUE，否則為 **VARIANT \_** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                    |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                                                       |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器 (VM) 必須針對此操作執行。<br/>                     |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 客體作業系統中未啟用 [整合元件] 功能。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

