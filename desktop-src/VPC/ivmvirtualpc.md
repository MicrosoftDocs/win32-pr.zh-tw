---
title: 'IVMVirtualPC 介面 (VPCCOMInterfaces .h) '
description: 定義頂層 Windows Virtual PC 應用程式物件。 所有其他 Windows 的 Virtual PC 介面物件都會透過此物件抓取。
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- IVMVirtualPC 介面 Virtual PC
- IVMVirtualPC 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69dd5eec832e95b2b93ff0fb0bee026428a937fa277f86ff14ef672bc66e0dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124648"
---
# <a name="ivmvirtualpc-interface"></a>IVMVirtualPC 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義頂層 Windows Virtual PC 應用程式物件。 所有其他 Windows 的 Virtual PC 介面物件都會透過此物件抓取。

**IVMVirtualPC** 可以使用 [**IVMVirtualPCEvents**](ivmvirtualpcevents.md) 輸出介面，通知用戶端有關事件的資訊。

## <a name="members"></a>成員

**IVMVirtualPC** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualPC** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMVirtualPC** 介面具有這些方法。



| 方法                                                                                      | 描述                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | 建立差異虛擬硬碟。<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | 建立動態調整大小的虛擬硬碟。<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | 建立固定大小的虛擬硬碟。<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | 建立磁片影像檔案。<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | 建立新的虛擬機器設定，並捕獲虛擬機器物件。<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | 刪除虛擬機器設定。<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | 抓取符合所要求設定的虛擬機器物件。<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | 抓取符合所要求名稱的虛擬網路物件。<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | 擷取指定之組態設定的值。<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | 捕獲已知 DVD 檔案的陣列。<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | 捕獲已知虛擬磁片檔案的陣列。<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | 抓取現有磁片影像檔的類型。<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | 抓取對應于現有磁片影像檔案的物件。<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | 捕獲已知虛擬硬碟檔案的陣列。<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | 捕獲已知虛擬機器組態檔的陣列。<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | 註冊現有的虛擬機器設定，並抓取虛擬機器物件。<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | 移除指定之設定的值。<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | 設定指定之設定的值。<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | 取消註冊虛擬機器設定，而不刪除設定檔。<br/>          |



 

### <a name="properties"></a>屬性

**IVMVirtualPC** 介面具有這些屬性。



| 屬性                                                                                   | 存取類型           | 描述                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | 讀取/寫入<br/> | 要搜尋可用虛擬機器組態檔案的預設目錄。<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | 唯讀<br/>  | 實體電腦的相關資訊。<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | 唯讀<br/>  | 每部虛擬機器的最大磁片磁碟機數目。<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | 唯讀<br/>  | 每部虛擬機器的最大可允許實體記憶體數量（以 mb 為單位）。<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | 唯讀<br/>  | 每個虛擬機器的網路介面數目上限。<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | 唯讀<br/>  | IDE 允許的最大匯流排數目。<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | 唯讀<br/>  | 每個虛擬機器的最大平行埠數目。<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | 唯讀<br/>  | 每個虛擬機器的序列埠數目上限。<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | 唯讀<br/>  | 每個虛擬機器的最小可允許實體記憶體數量（以 mb 為單位）。<br/>                                                       |
| [**名稱**](ivmvirtualpc-name.md)<br/>                                               | 唯讀<br/>  | Windows Virtual PC 應用程式的名稱。<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | 讀取/寫入<br/> | 用來尋找與 Windows Virtual PC 相關聯之檔案的檔案系統路徑。<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | 唯讀<br/>  | 每個虛擬機器的最大可允許實體記憶體數量（以 mb 為單位），以避免主機上的記憶體不足狀況。<br/> |
| [**工作**](ivmvirtualpc-tasks.md)<br/>                                             | 唯讀<br/>  | 工作的集合。<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | 唯讀<br/>  | 未連接之網路介面的可列舉集合。<br/>                                                                                |
| [**99.99**](ivmvirtualpc-uptime.md)<br/>                                           | 唯讀<br/>  | Windows Virtual PC 應用程式執行的秒數。<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | 唯讀<br/>  | 所有連接至主機之 USB 裝置的可列舉集合。<br/>                                                                         |
| [**版本**](ivmvirtualpc-version.md)<br/>                                         | 唯讀<br/>  | 此 Windows Virtual PC 實例的版本。<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | 唯讀<br/>  | 虛擬機器的可列舉集合。<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | 唯讀<br/>  | 虛擬網路的可列舉集合。<br/>                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



 

