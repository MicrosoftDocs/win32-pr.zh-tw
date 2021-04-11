---
title: 'IVMFloppyDrive 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的軟碟磁碟機。
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- IVMFloppyDrive 介面 Virtual PC
- IVMFloppyDrive 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934929"
---
# <a name="ivmfloppydrive-interface"></a>IVMFloppyDrive 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

控制虛擬機器內的軟碟磁碟機。 **IVMFloppyDrive** 可以使用 [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) 的輸出介面，通知用戶端有關事件的資訊。 您可以從 [**IVMVirtualMachine：： FloppyDrives**](ivmvirtualmachine-floppydrives.md)屬性傳回的 [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)物件中取出 **IVMFloppyDrive** 物件。

## <a name="members"></a>成員

**IVMFloppyDrive** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMFloppyDrive** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMFloppyDrive** 介面具有這些方法。



| 方法                                                      | 描述                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AttachHostDrive**](ivmfloppydrive-attachhostdrive.md)   | 將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。<br/> |
| [**AttachImage**](ivmfloppydrive-attachimage.md)           | 將主機上的軟碟媒體映射連接到磁片磁碟機。<br/>                    |
| [**ReleaseHostDrive**](ivmfloppydrive-releasehostdrive.md) | 從軟碟磁碟機釋放主機上的實體磁片磁碟機。<br/>                      |
| [**ReleaseImage**](ivmfloppydrive-releaseimage.md)         | 從軟碟磁碟機釋放主機上的軟碟媒體映射。<br/>                  |



 

### <a name="properties"></a>屬性

**IVMFloppyDrive** 介面具有這些屬性。



| 屬性                                                             | 存取類型          | Description                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**附件**](ivmfloppydrive-attachment.md)<br/>           | 唯讀<br/> | 連接至虛擬機器中之磁片磁碟機的媒體類型。<br/>     |
| [**DriveNumber**](ivmfloppydrive-drivenumber.md)<br/>         | 唯讀<br/> | 連接此磁片磁碟機之控制器的以零為起始的索引。<br/> |
| [**HostDriveLetter**](ivmfloppydrive-hostdriveletter.md)<br/> | 唯讀<br/> | 連接軟碟磁碟機的主機磁片磁碟機的字母。<br/>            |
| [**映射檔**](ivmfloppydrive-imagefile.md)<br/>             | 唯讀<br/> | 連接軟碟磁碟機之影像檔案的完整路徑。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



 

