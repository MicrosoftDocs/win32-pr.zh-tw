---
title: 'IVMVirtualMachine 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器的介面。
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- IVMVirtualMachine 介面 Virtual PC
- IVMVirtualMachine 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2f50c5279bafd12d8edd01a47e9cbcb1a3cc3bb2b89ea140e46cf06c0aa06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124678"
---
# <a name="ivmvirtualmachine-interface"></a>IVMVirtualMachine 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器的介面。 **IVMVirtualMachine** 可以使用 [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) 的輸出介面，通知用戶端有關事件的資訊。 **IVMVirtualMachine** 物件會從 [**IVMVirtualPC**](ivmvirtualpc.md) 方法（例如 [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)、 [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)和 [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)）傳回。 您也可以從 [**IVMVirtualPC：： VirtualMachines**](ivmvirtualpc-virtualmachines.md)屬性傳回的 [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)物件中取出 **IVMVirtualMachine** 物件。

## <a name="members"></a>成員

**IVMVirtualMachine** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualMachine** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMVirtualMachine** 介面具有這些方法。



| 方法                                                                           | 描述                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | 將新的 CD 或 DVD 光碟機新增至虛擬機器。<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | 將新的硬碟連接新增至虛擬機器。<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | 將網路介面新增至虛擬機器。<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | 將 USB 裝置連接到虛擬機器。<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | 從虛擬機器釋放 USB 裝置。<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | 捨棄已儲存之虛擬機器的任何儲存狀態資訊。<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | 捨棄虛擬復原磁片。<br/>                                                                |
| [**GetActivationValue**](ivmvirtualmachine-getactivationvalue.md)               | 抓取此虛擬機器之指定啟用設定的值。<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | 抓取此虛擬機器的指定設定設定值。<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | 合併虛擬復原磁片。<br/>                                                                  |
| [**暫停**](ivmvirtualmachine-pause.md)                                         | 暫停虛擬機器。<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | 移除此虛擬機器之指定啟用設定的值。<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | 移除此虛擬機器的指定設定設定值。<br/>              |
| [**RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | 從虛擬機器移除指定的 CD 或 DVD 光碟機。<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | 從虛擬機器移除指定的硬碟連接。<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | 從虛擬機器移除網路介面。<br/>                                           |
| [**重設**](ivmvirtualmachine-reset.md)                                         | 重設虛擬機器。<br/>                                                                     |
| [**繼續**](ivmvirtualmachine-resume.md)                                       | 繼續虛擬機器。<br/>                                                                    |
| [**儲存**](ivmvirtualmachine-save.md)                                           | 儲存虛擬機器狀態。<br/>                                                                |
| [**SetActivationValue**](ivmvirtualmachine-setactivationvalue.md)               | 為此虛擬機器設定指定之啟用設定的值。<br/>                    |
| [**SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)         | 設定此虛擬機器之指定設定的值。<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | 設定主機與來賓之間的通道。<br/>                                         |
| [**啟動**](ivmvirtualmachine-startup.md)                                     | 從未初始化或已儲存的狀態啟動虛擬機器。<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | 使用 advanced 選項，從未初始化或已儲存的狀態啟動虛擬機器。<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | 關閉虛擬機器。<br/>                                                                  |



 

### <a name="properties"></a>屬性

**IVMVirtualMachine** 介面具有這些屬性。



| 屬性                                                                            | 存取類型           | 描述                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**會計**](ivmvirtualmachine-accountant.md)<br/>                       | 唯讀<br/>  | 此虛擬機器的會計。<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | 唯讀<br/>  | 陣列，指出連接到虛擬機器中每個位置的磁片磁碟機類型。<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | 讀取/寫入<br/> | 基本板序號。<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | 讀取/寫入<br/> | BIOS GUID。<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | 讀取/寫入<br/> | BIOS 序號。<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | 讀取/寫入<br/> | 底座資產標記。<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | 讀取/寫入<br/> | 底座序號。<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | 唯讀<br/>  | 虛擬機器的唯一識別碼。<br/>                                                                                      |
| [**顯示**](ivmvirtualmachine-display.md)<br/>                             | 唯讀<br/>  | 虛擬機器的影片顯示。<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | 唯讀<br/>  | 連接至虛擬機器之 CD 和 DVD 光碟機的可列舉集合。<br/>                                                      |
| [**檔案**](ivmvirtualmachine-file.md)<br/>                                   | 唯讀<br/>  | 虛擬機器設定之 .vmc 檔案的完整路徑。<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | 唯讀<br/>  | 連接至虛擬機器之軟碟磁碟機的可列舉集合。<br/>                                                          |
| [**GuestOS**](ivmvirtualmachine-guestos.md)<br/>                             | 唯讀<br/>  | 此虛擬機器的客體作業系統。<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | 唯讀<br/>  | 硬碟連接的可列舉集合。<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | 唯讀<br/>  | 指出處理器是否支援3DNow 指令集。<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | 唯讀<br/>  | 指出處理器是否支援 MMX 指令集。<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | 唯讀<br/>  | 指出處理器是否支援 SSE 指令集。<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | 唯讀<br/>  | 指出處理器是否支援 SSE2 指令集。<br/>                                                                  |
| [**鍵盤**](ivmvirtualmachine-keyboard.md)<br/>                           | 唯讀<br/>  | 虛擬機器的鍵盤裝置。<br/>                                                                                        |
| [**記憶**](ivmvirtualmachine-memory.md)<br/>                               | 讀取/寫入<br/> | 虛擬機器中的實體記憶體數量（以 mb 為單位）。<br/>                                                                 |
| [**滑鼠**](ivmvirtualmachine-mouse.md)<br/>                                 | 唯讀<br/>  | 虛擬機器的滑鼠裝置。<br/>                                                                                           |
| [**名稱**](ivmvirtualmachine-name.md)<br/>                                   | 讀取/寫入<br/> | 虛擬機器設定的名稱。<br/>                                                                                      |
| [**NetworkAdapters**](ivmvirtualmachine-networkadapters.md)<br/>             | 唯讀<br/>  | 連接至虛擬機器之 Nic 的可列舉集合。<br/>                                                                   |
| [**備註**](ivmvirtualmachine-notes.md)<br/>                                 | 讀取/寫入<br/> | 虛擬機器的附注。<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | 唯讀<br/>  | 平行埠的可列舉集合。<br/>                                                                                         |
| [**>processorspeed**](ivmvirtualmachine-processorspeed.md)<br/>               | 唯讀<br/>  | 處理器的速度，以 MHz (MHz) 。<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | 唯讀<br/>  | 用於影片和輸入的 RDP 連接具名管道的名稱。<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | 唯讀<br/>  | 儲存狀態檔案的完整路徑。<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | 唯讀<br/>  | 序列埠的可列舉集合。<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | 讀取/寫入<br/> | 當 Windows virtual PC 結束時，要在此虛擬機器上執行的動作。<br/>                                |
| [**狀態**](ivmvirtualmachine-state.md)<br/>                                 | 唯讀<br/>  | 虛擬機器的目前狀態。<br/>                                                                                           |
| [**撤銷**](ivmvirtualmachine-undoable.md)<br/>                           | 讀取/寫入<br/> | 指出是否已為連接至虛擬機器的硬碟啟用復原磁片磁碟機。<br/>                                      |
| [**UndoAction**](ivmvirtualmachine-undoaction.md)<br/>                       | 讀取/寫入<br/> | 當虛擬機器從客體作業系統中關閉時，要在所有復原磁片磁碟機上執行的預設動作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



 

