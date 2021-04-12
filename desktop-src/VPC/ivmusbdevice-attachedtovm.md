---
title: 'IVMUSBDevice AttachedToVM 屬性 (VPCCOMInterfaces .h) '
description: 抓取 USB 裝置所連接之虛擬機器的名稱。
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- AttachedToVM 屬性 Virtual PC
- AttachedToVM 屬性 Virtual PC，IVMUSBDevice 介面
- IVMUSBDevice 介面 Virtual PC，AttachedToVM 屬性
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025164"
---
# <a name="ivmusbdeviceattachedtovm-property"></a>IVMUSBDevice：： AttachedToVM 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取 USB 裝置所連接之虛擬機器的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>屬性值

虛擬機器 (VM) 的名稱。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                           | 意義                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                              | 裝置會連接到 VM，並傳回其名稱。<br/> |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                           | 裝置已附加至主機。<br/>                         |
| <dl> <dt>VM \_E \_ USB \_ 外部 \_ VM</dt> <dt>0xA00400929</dt> </dl> | 裝置會附加至另一個使用者會話中的 VM。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                | 參數為 **Null**。<br/>                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

