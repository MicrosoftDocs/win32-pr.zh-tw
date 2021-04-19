---
title: 'IVMUSBDevice 介面 (VPCCOMInterfaces .h) '
description: 定義連接至主機之 USB 裝置的介面。 您可以將 USB 裝置連接到虛擬機器，以在虛擬機器中使用該裝置。
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- IVMUSBDevice 介面 Virtual PC
- IVMUSBDevice 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968351"
---
# <a name="ivmusbdevice-interface"></a>IVMUSBDevice 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義連接至主機之 USB 裝置的介面。 您可以將 USB 裝置連接到虛擬機器，以在虛擬機器中使用該裝置。

## <a name="members"></a>成員

**IVMUSBDevice** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMUSBDevice** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMUSBDevice** 介面具有這些屬性。



| 屬性                                                                 | 存取類型          | Description                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**AttachedToVM**](ivmusbdevice-attachedtovm.md)<br/>             | 唯讀<br/> | USB 裝置所連接之虛擬機器的名稱。<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | 唯讀<br/> | USB 裝置的裝置類別。<br/>                                  |
| [**DeviceString**](ivmusbdevice-devicestring.md)<br/>             | 唯讀<br/> | USB 裝置的名稱。<br/>                                          |
| [**HubID**](ivmusbdevice-hubid.md)<br/>                           | 唯讀<br/> | 裝置所連接之中樞的識別碼。<br/>          |
| [**ManufacturerString**](ivmusbdevice-manufacturerstring.md)<br/> | 唯讀<br/> | USB 裝置製造商的名稱。<br/>                             |
| [**連接埠**](ivmusbdevice-port.md)<br/>                             | 唯讀<br/> | 裝置所連接之埠的識別碼。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



 

