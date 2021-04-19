---
description: 存放裝置物件分成三種類型：控制器、磁片磁碟機和媒體。
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: 儲存類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c17ad2530a86e7f404fe19eaeb3ef5a1cd7895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975877"
---
# <a name="storage-classes"></a>儲存類別

存放裝置物件分成三種類型：控制器、磁片磁碟機和媒體。

有兩個控制器：模擬的 IDE 控制器和綜合 SCSI 控制器。 這兩個控制器都支援裝載媒體之磁片磁碟機的附件。

以下是與儲存體相關的虛擬化 WMI 類別。 此外，也支援綜合磁片媒體。 不支援連接到實體磁片磁碟機。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                      | 描述                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | 表示作業與受管理元素之間的關聯，這些專案可能會受其執行影響。<br/>                                                                                               |
| [**Msvm \_ BasedOn**](msvm-basedon.md)<br/>                                           | 描述如何從較低層級範圍組合儲存區範圍的關聯。<br/>                                                                                                           |
| [**Msvm \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | 將存放裝置與擁有裝置的儲存控制器產生關聯。<br/>                                                                                                                          |
| [**Msvm \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | 代表虛擬機器內的硬碟。<br/>                                                                                                                                              |
| [**Msvm \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | 代表虛擬機器中的軟碟控制卡。<br/>                                                                                                                                               |
| [**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | 代表虛擬機器內的磁片磁碟機。<br/>                                                                                                                                                  |
| [**Msvm \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | 代表虛擬機器內的 DVD 光碟機。<br/>                                                                                                                                                    |
| [**Msvm \_ IDEController**](msvm-idecontroller.md)<br/>                               | 代表 IDE 控制器。<br/>                                                                                                                                                                          |
| [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | 管理虛擬機器的虛擬媒體 ( .vhd、.vhdx、.iso 或 .vfd 檔案) 。<br/>                                                                                                                    |
| [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)<br/>                                   | 代表存放磁片磁碟機媒體，用來填入存放磁片磁碟機。<br/>                                                                                                                             |
| [**Msvm \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | 將存放磁片磁碟機與插入磁片磁碟機的媒體產生關聯。<br/>                                                                                                                                     |
| [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | 提供有關手動掛接之儲存體映射的詳細資訊。<br/>                                                                                                                                  |
| [**Msvm \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | 此關聯表示邏輯裝置的子類別 (例如，存放磁片區) 透過特定的通訊協定控制器連線。<br/>                                                       |
| [**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | 代表綜合 SCSI 控制器。<br/>                                                                                                                                                                |
| [**Msvm \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | 代表每次 [**Msvm \_ ResourcePool**](msvm-resourcepool.md)或 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)類別的 **OperationalStatus** 屬性變更時引發的事件。<br/> |
| [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | 表示與虛擬儲存體配置特別相關的設定。<br/>                                                                                                                         |
| [**Msvm \_ get-storagejob**](msvm-storagejob.md)<br/>                                     | 代表 Microsoft Hyper-V 映射管理服務所建立的儲存體作業工作。<br/>                                                                                                          |
| [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | 提供虛擬硬碟的設定資料。<br/>                                                                                                                                                         |
| [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | 提供現有虛擬硬碟映射的狀態資訊。<br/>                                                                                                                                    |



 

 

 




