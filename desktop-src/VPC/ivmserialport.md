---
title: 'IVMSerialPort 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的序列埠。
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- IVMSerialPort 介面 Virtual PC
- IVMSerialPort 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508987"
---
# <a name="ivmserialport-interface"></a>IVMSerialPort 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內的序列埠。 此介面可讓您設定虛擬機器內的序列埠。 您可以從 [**IVMVirtualMachine：： serialport**](ivmvirtualmachine-serialports.md)屬性傳回的 [**IVMSerialPortCollection**](ivmserialportcollection.md)物件中取出 **IVMSerialPort** 物件。

## <a name="members"></a>成員

**IVMSerialPort** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMSerialPort** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMSerialPort** 介面具有這些方法。



| 方法                                       | 描述                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_ID**](ivmserialport--id.md)            | 捕獲序列埠的內部識別碼。<br/> |
| [**設定**](ivmserialport-configure.md) | 設定序列埠。<br/>                           |



 

### <a name="properties"></a>屬性

**IVMSerialPort** 介面具有這些屬性。



| 屬性                                                                  | 存取類型          | Description                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | 唯讀<br/> | 指出是否應該在不等候數據機命令的情況下開啟序列埠。<br/> |
| [**Name**](ivmserialport-name.md)<br/>                             | 唯讀<br/> | 序列埠的名稱。<br/>                                                                           |
| [**類型**](ivmserialport-type.md)<br/>                             | 唯讀<br/> | 序列埠的型別。<br/>                                                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



 

