---
title: 'IVMHardDiskConnection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內硬碟的連接。
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- IVMHardDiskConnection 介面 Virtual PC
- IVMHardDiskConnection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8522a6f8c24f2f80728a878435b42ac4179432e1cca4234feb29261fe2c11f8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510788"
---
# <a name="ivmharddiskconnection-interface"></a>IVMHardDiskConnection 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內硬碟的連接。 從 [**IVMVirtualMachine：： AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)方法傳回的 **IVMHardDiskConnection** 物件。 您也可以從 [**IVMVirtualMachine：： HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)屬性傳回的 [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)物件中取出 **IVMHardDiskConnection** 物件。

## <a name="members"></a>成員

**IVMHardDiskConnection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMHardDiskConnection** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMHardDiskConnection** 介面具有這些方法。



| 方法                                                         | 描述                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | 設定此硬碟所連接的匯流排位置。<br/> |



 

### <a name="properties"></a>屬性

**IVMHardDiskConnection** 介面具有這些屬性。



| 屬性                                                              | 存取類型          | 描述                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | 唯讀<br/> | 磁片磁碟機映射所連接的匯流排編號。<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | 唯讀<br/> | 磁片磁碟機映射所連接的裝置編號。<br/>                |
| [**硬碟**](ivmharddiskconnection-harddisk.md)<br/>         | 唯讀<br/> | 對應至此連接的硬碟物件。<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | 唯讀<br/> | 與此連線的復原磁片映射對應的硬碟物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



 

