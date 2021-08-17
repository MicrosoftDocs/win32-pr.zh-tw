---
title: 'IVMVirtualPC USBDeviceCollection 屬性 (VPCCOMInterfaces .h) '
description: 所有連接至主機之 USB 裝置的可列舉集合。
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- USBDeviceCollection 屬性 Virtual PC
- USBDeviceCollection 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，USBDeviceCollection 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2880a6f7adb60605e37fe78481613016d17fdbbd2e27f1a6add4ce031030deea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136521"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>IVMVirtualPC：： USBDeviceCollection 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取所有連接至主機之 USB 裝置的可列舉集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>屬性值

[**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)指標的參考，代表 [**IVMUSBDevice**](ivmusbdevice.md)物件的集合。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                                | 意義                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                   | 作業成功。<br/>                                                        |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                     | 參數為 **Null**。<br/>                                                           |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                             | 已發生未預期的錯誤。<br/>                                                    |
| <dl> <dt>VM \_E \_ USB \_ 列舉 \_ 失敗 \_ 的 \_ 裝置更多</dt> <dt>0xA0040930</dt> </dl> | 有16個以上的 USB 裝置連接到主機。<br/>                                  |
| <dl> <dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt> </dl>      | 處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。<br/> |



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

 

