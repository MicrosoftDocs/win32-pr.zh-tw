---
title: 'IVMUSBDeviceCollection 介面 (VPCCOMInterfaces .h) '
description: 定義連接至主機系統的 USB 裝置集合。 若要取得 IVMUSBDeviceCollection 物件，請使用 IVMVirtualPC USBDeviceCollection 屬性。
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- IVMUSBDeviceCollection 介面 Virtual PC
- IVMUSBDeviceCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752537"
---
# <a name="ivmusbdevicecollection-interface"></a>IVMUSBDeviceCollection 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義連接至主機系統的 USB 裝置集合。 若要取得 **IVMUSBDeviceCollection** 物件，請使用 [**IVMVirtualPC：： USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) 屬性。

## <a name="members"></a>成員

**IVMUSBDeviceCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMUSBDeviceCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMUSBDeviceCollection** 介面具有這些屬性。



| 屬性                                                        | 存取類型          | 描述                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                        |
| [**計數**](ivmusbdevicecollection-count.md)<br/>        | 唯讀<br/> | 此集合中的 USB 裝置數目。<br/>                            |
| [**項目**](ivmusbdevicecollection-item.md)<br/>          | 唯讀<br/> | 對應至指定索引 (1) 的 USB 裝置物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection 定義為4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

