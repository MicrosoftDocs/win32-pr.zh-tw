---
title: 'IVMVirtualMachine AttachUSBDevice 方法 (VPCCOMInterfaces .h) '
description: 將 USB 裝置連接至 VM。
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice 方法 Virtual PC
- AttachUSBDevice 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AttachUSBDevice 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006898"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>IVMVirtualMachine：： AttachUSBDevice 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將 USB 裝置連接到 (VM) 的虛擬機器。

## <a name="syntax"></a>語法


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inUSBDevice* \[在\]
</dt> <dd>

[**IVMUSBDevice**](ivmusbdevice.md)指標，表示連接至主機的 USB 裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                             | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                   | 作業成功。<br/>                                           |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                     | 參數為 **Null**。<br/>                                              |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                        | VM 未執行。<br/>                                                  |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                             | 未知的設定。<br/>                                           |
| <dl> <dt>**VM \_E \_ 新增 \_ 專案 \_ 無法**</dt> <dt>0xA0040504</dt> </dl>                   | 在客體作業系統中無法使用整合元件。<br/> |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl>          | USB 功能無法使用。<br/>                                       |
| <dl> <dt>**VM \_E \_ USB \_ 連接器 \_ 驅動程式 \_ 錯誤**</dt> <dt>0xA00400925</dt> </dl>          | 發生 USB 連接器驅動程式錯誤。<br/>                                 |
| <dl> <dt>**VM \_E \_ USB \_ 附加 \_ 失敗 \_ 的 \_ 裝置**</dt> <dt>0xA00400931</dt> </dl>     | 無法將更多裝置連結至 VM。<br/>                                   |
| <dl> <dt>**VM \_E \_ USB \_ 附加 \_ 失敗的 \_ GP \_ 錯誤**</dt> <dt>0xA00400932</dt> </dl>         | 群組原則設定阻礙了 USB 重新導向。<br/>               |
| <dl> <dt>**VM \_E \_ USB \_ 附加 \_ 失敗 \_ 已 \_ 指派**</dt> <dt>0xA00400933</dt> </dl> | 已有其他用戶端連接 USB 裝置。<br/>            |
| <dl> <dt>**VM \_E \_ USB \_ 附加 \_ 失敗**</dt> <dt>0xA00400926</dt> </dl>                    | 附加作業失敗。<br/>                                            |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                             | 已發生未預期的錯誤。<br/>                                       |



 

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

 

