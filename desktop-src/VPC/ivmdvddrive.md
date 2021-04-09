---
title: 'IVMDVDDrive 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的 CD-ROM 或 DVD-ROM 光碟機。 IVMDVDDrive 可以使用 IVMDVDDriveEvents 的輸出介面，通知用戶端有關事件的資訊。
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- IVMDVDDrive 介面 Virtual PC
- IVMDVDDrive 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025232"
---
# <a name="ivmdvddrive-interface"></a>IVMDVDDrive 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

控制虛擬機器內的 CD-ROM 或 DVD-ROM 光碟機。 **IVMDVDDrive** 可以使用 [**IVMDVDDriveEvents**](ivmdvddriveevents.md) 的輸出介面，通知用戶端有關事件的資訊。

您可以使用 [**IVMVirtualMachine：： AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) 方法，將新的 CD-ROM 或 dvd-rom 光碟機新增至虛擬機器。 您可以使用 [**IVMVirtualMachine：： RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) 方法，從虛擬機器移除現有的 CD-ROM 或 dvd-rom 光碟機。 您可以從 [**IVMVirtualMachine：:D vdromdrives**](ivmvirtualmachine-dvdromdrives.md)屬性傳回的 [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)物件中取出 **IVMDVDDrive** 物件。

## <a name="members"></a>成員

**IVMDVDDrive** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMDVDDrive** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMDVDDrive** 介面具有這些方法。



| 方法                                                   | 描述                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmdvddrive-attachhostdrive.md)   | 將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。<br/>           |
| [**AttachImage**](ivmdvddrive-attachimage.md)           | 將 ISO 映像連接到虛擬機器中的 DVD 光碟機。<br/>           |
| [**ReleaseHostDrive**](ivmdvddrive-releasehostdrive.md) | 從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。<br/>                           |
| [**ReleaseImage**](ivmdvddrive-releaseimage.md)         | 從 DVD 光碟機釋放已捕獲的 ISO 映像。<br/>                            |
| [**SetBusLocation**](ivmdvddrive-setbuslocation.md)     | 將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。<br/> |



 

### <a name="properties"></a>屬性

**IVMDVDDrive** 介面具有這些屬性。



| 屬性                                                          | 存取類型          | Description                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**附件**](ivmdvddrive-attachment.md)<br/>           | 唯讀<br/> | 連接至虛擬機器內 DVD 光碟機的媒體類型。<br/> |
| [**BusNumber**](ivmdvddrive-busnumber.md)<br/>             | 唯讀<br/> | 此裝置所連接的匯流排號碼。<br/>                        |
| [**DeviceNumber**](ivmdvddrive-devicenumber.md)<br/>       | 唯讀<br/> | 此磁片磁碟機所連接的裝置編號。<br/>                      |
| [**HostDriveLetter**](ivmdvddrive-hostdriveletter.md)<br/> | 唯讀<br/> | 為此裝置設定之主機磁片磁碟機的字母。<br/>                       |
| [**映射檔**](ivmdvddrive-imagefile.md)<br/>             | 唯讀<br/> | 為此裝置設定之影像檔案的完整路徑。<br/>                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



 

