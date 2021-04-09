---
description: 電腦系統硬體類別會將代表硬體相關物件的類別群組在一起。 範例包括輸入裝置、硬碟、擴充卡、影片裝置、網路裝置和系統電源。
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: 電腦系統硬體類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936306"
---
# <a name="computer-system-hardware-classes"></a>電腦系統硬體類別

電腦系統硬體類別會將代表硬體相關物件的類別群組在一起。 範例包括輸入裝置、硬碟、擴充卡、影片裝置、網路裝置和系統電源。

-   [冷卻裝置類別](#cooling-device-classes)
-   [輸入裝置類別](#input-device-classes)
-   [大量儲存類別](#mass-storage-classes)
-   [主機板、控制器和埠類別](#motherboard-controller-and-port-classes)
-   [網路裝置類別](#networking-device-classes)
-   [Power 類別](#power-classes)
-   [列印類別](#printing-classes)
-   [電話語音類別](#telephony-classes)
-   [影片和監視類別](#video-and-monitor-classes)
-   [相關主題](#related-topics)

## <a name="cooling-device-classes"></a>冷卻裝置類別

冷卻裝置子類別會將代表 instrumentable 風扇、溫度探查和冷藏庫取出裝置的類別分組。



| 類別                                                     | 描述                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Win32 \_ 風扇**](win32-fan.md)                           | 代表電腦系統中的風扇裝置屬性。           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | 代表熱度管道冷卻裝置的屬性。                    |
| [**Win32 \_ 冷藏庫取出**](win32-refrigeration.md)       | 代表冷藏庫取出裝置的屬性。                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | 代表溫度感應器的屬性 (電子溫度計) 。 |



 

## <a name="input-device-classes"></a>輸入裝置類別

輸入裝置子類別會將代表鍵盤和指標裝置的類別分組。



| 類別                                                 | 描述                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 鍵盤**](win32-keyboard.md)             | 代表安裝在執行 Windows 之電腦系統上的鍵盤。                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | 代表輸入裝置，用來在顯示執行 Windows 的電腦系統時，指向並選取區域。 |



 

## <a name="mass-storage-classes"></a>大量儲存類別

大量儲存子類別中的類別代表存放裝置，例如硬碟機、CD-ROM 光碟機和磁帶機。



| 類別                                                     | 描述                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ AutochkSetting**](win32-autochksetting.md)     | 代表磁片的 autocheck 操作設定。                               |
| [**Win32 \_ CDROMDrive**](win32-cdromdrive.md)             | 代表執行 Windows 的電腦系統上的 CD-ROM 光碟機。                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | 代表執行 Windows 作業系統的電腦所見的實體磁片磁碟機。 |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | 管理軟碟磁碟機的功能。                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | 代表任何類型的檔或儲存媒體。                                      |
| [**Win32 \_ disable-tapedrive**](win32-tapedrive.md)               | 代表電腦系統上執行 Windows 的磁帶機。                                |



 

## <a name="motherboard-controller-and-port-classes"></a>主機板、控制器和埠類別

主機板、控制器和埠子類別會群組代表系統裝置的類別。 範例包括系統記憶體、快取記憶體和控制器。



| 類別                                                                       | 描述                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | 代表1394控制器的功能和管理。<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | 建立高速串列匯流排 (IEEE 1394 Firewire) 控制器以及與其連接的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例的關聯。<br/>                                                            |
| [**Win32 \_ AllocatedResource**](win32-allocatedresource.md)                 | 將邏輯裝置與系統資源建立關聯。<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | 使處理器與其快取記憶體產生關聯。<br/>                                                                                                                                                                      |
| [**Win32 \_ 基礎板**](win32-baseboard.md)                                 | 代表基礎板 (也稱為主機板或系統面板) 。<br/>                                                                                                                                          |
| [**Win32 \_ BIOS**](win32-bios.md)                                           | 代表電腦上安裝的電腦系統基本輸入或輸出服務 (BIOS) 的屬性。<br/>                                                                                   |
| [**Win32 \_ 匯流排**](win32-bus.md)                                             | 代表 Windows 作業系統所見的實體匯流排。<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | 代表電腦系統上 (內部和外部) 的快取記憶體。<br/>                                                                                                                                          |
| [**Win32 \_ ControllerHasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | 表示從通用序列匯流排 (USB) 控制器下游的中樞。<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | 使用匯流排建立系統匯流排和邏輯裝置的關聯。<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | 代表 Windows 系統上的裝置記憶體位址。<br/>                                                                                                                                                        |
| [**Win32 \_ DeviceSettings**](win32-devicesettings.md)                       | 使邏輯裝置和可以套用的設定產生關聯。<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | 表示在執行 Windows 的電腦系統上 (DMA) 通道的直接記憶體存取許可權。<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | 代表軟碟磁碟機控制器的功能和管理能力。<br/>                                                                                                                         |
| [**Win32 \_ IDEController**](win32-idecontroller.md)                         | 代表整合式裝置電子 (IDE) 控制器裝置的功能。<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | 關聯至 IDE 控制器和邏輯裝置的關聯類別。<br/>                                                                                                                                       |
| [**Win32 \_ InfraredDevice**](win32-infrareddevice.md)                       | 代表紅外線裝置的功能和管理。<br/>                                                                                                                                              |
| [**Win32 \_ IRQResource**](win32-irqresource.md)                             | 代表 Windows 電腦系統上 (IRQ) 號碼的插斷要求行。<br/>                                                                                                                                |
| [**Win32 \_ MemoryArray**](win32-memoryarray.md)                             | 代表電腦系統記憶體陣列和對應位址的屬性。<br/>                                                                                                                            |
| [**Win32 \_ MemoryArrayLocation**](win32-memoryarraylocation.md)             | 將邏輯記憶體陣列和其所在的實體記憶體陣列產生關聯。<br/>                                                                                                                             |
| [**Win32 \_ MemoryDevice**](win32-memorydevice.md)                           | 代表電腦系統記憶體裝置的屬性以及其相關聯的對應位址。<br/>                                                                                                     |
| [**Win32 \_ MemoryDeviceArray**](win32-memorydevicearray.md)                 | 將記憶體裝置和其所在的記憶體陣列產生關聯。<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | 關聯性類別，其會將記憶體裝置與其存在的實體記憶體相關聯。<br/>                                                                                                                     |
| [**Win32 \_ MotherboardDevice**](win32-motherboarddevice.md)                 | 代表包含執行 Windows 之電腦系統中央元件的裝置。<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | 代表內建于主機板 (系統面板) 內建的通用介面卡裝置。<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | 表示在執行 Windows 的電腦系統上的平行埠屬性。<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | 管理個人電腦記憶卡介面介面卡 (PCMCIA) 控制器裝置的功能。<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | 代表位於電腦上的實體記憶體裝置，可供作業系統使用。<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | 代表電腦系統實體記憶體的詳細資料。<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | 將實體記憶體和其實體記憶體的陣列產生關聯。<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | 代表邏輯裝置和系統資源之間的關聯。<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | 將已知的裝置 (設定管理員 PNPEntity) ，以及它所執行的函式建立關聯。<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | 代表隨插即用裝置的屬性。<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | 代表實體連線埠，例如 DB-25 針腳男性、Centronics 和 PS/2。<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | 代表執行 Windows 的電腦系統上的 i/o 埠。<br/>                                                                                                                                                   |
| [**Win32 \_ 處理器**](win32-processor.md)                                 | 代表能夠在執行 Windows 的電腦系統上解讀一連串電腦指令的裝置。<br/>                                                                                           |
| [**Win32 \_ microsoft.hyperv.powershell.scsicontroller**](win32-scsicontroller.md)                       | 表示在執行 Windows 的電腦系統上 (SCSI) 控制器的小型電腦系統介面。<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | 將 SCSI 控制器與邏輯裝置 (磁片磁碟機) 連接到該磁片磁碟機。<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | 代表執行 Windows 的電腦系統上的序列埠。<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | 代表 Windows 序列埠上資料傳輸的設定。<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | 建立序列埠及其設定的關聯。<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | 代表記憶體相關邏輯裝置的功能和管理。<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | 代表執行 Windows 的電腦系統上的音效裝置內容。<br/>                                                                                                                              |
| [**Win32 \_ SystemBIOS**](win32-systembios.md)                               | 將電腦系統 (包括啟動屬性、時區、開機設定或系統管理密碼等資料) 和系統 BIOS (服務、語言和系統管理屬性) 。<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | 將 Windows 電腦系統上的隨插即用裝置與支援隨插即用裝置的驅動程式相關聯。<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | 代表與實體系統主機殼相關聯的屬性。<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | 代表 Windows 系統上的系統記憶體資源。<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | 代表實體連接點，包括埠、主機板插槽和週邊設備，以及專屬的連接點。<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | 管理通用序列匯流排 (USB) 控制器的功能。<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | 建立 USB 控制器和與其連接的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例的關聯。<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | 代表 USB 集線器的管理特性。<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>網路裝置類別

網路裝置子類別會將代表網路介面控制器、其設定及其設定的類別分組。



| 類別                                                                           | 描述                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NetworkAdapter**](win32-networkadapter.md)                           | 代表執行 Windows 的電腦系統上的網路介面卡。<br/>                                                                                                                                          |
| [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md) | 代表網路介面卡的屬性和行為。 Ratification 分散式管理工作強制 (DMTF) CIM 網路規格之後，不保證會支援類別。<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | 建立網路介面卡及其設定的關聯。<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Power 類別

電源子類別目錄群組類別，代表與這些裝置相關的電源供應器、電池和事件。



| 類別                                                             | 描述                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 電池**](win32-battery.md)                           | 代表連接到電腦系統的電池。<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | 表示目前監視感應器 (ammeter) 的屬性。<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | 代表便攜電池的屬性，例如用於筆記本電腦的電池。<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | 代表電源狀態變更所產生的電源管理事件。<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | 代表電壓感應器的屬性 (電子電壓表) 。<br/>                      |



 

## <a name="printing-classes"></a>列印類別

列印子類別目錄會群組代表印表機、印表機設定和列印工作的類別。



| 類別                                                             | 描述                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | 將印表機與印表機驅動程式建立關聯。<br/>                                                                                        |
| [**Win32 \_ 印表機**](win32-printer.md)                           | 代表連接到執行 Windows 之電腦系統的裝置，該電腦可以在媒體上重新產生視覺影像。<br/> |
| [**Win32 \_ PrinterConfiguration**](win32-printerconfiguration.md) | 定義印表機裝置的設定。<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | 使印表機和印表機連線的本機裝置產生關聯。<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | 表示 [**Win32 \_ 印表機**](win32-printer.md) 實例的驅動程式。<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | 將本機印表機與其驅動程式檔案建立關聯， (不是驅動程式本身) 。<br/>                                                          |
| [**Win32 \_ PrinterSetting**](win32-printersetting.md)             | 建立印表機與其設定的關聯。<br/>                                                                             |
| [**Win32 \_ PrintJob**](win32-printjob.md)                         | 表示以 Windows 為基礎的應用程式所產生的列印工作。<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | 代表 TCP/IP 服務存取點。<br/>                                                                                     |



 

## <a name="telephony-classes"></a>電話語音類別

電話語音子類別會將代表「單純的電話」數據機裝置及其相關聯序列連接的類別分組。



| 類別                                                               | 描述                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ POTSModem**](win32-potsmodem.md)                         | 表示在執行 Windows 的電腦系統上， (POTS) 數據機的一般舊電話語音的服務和特性。<br/> |
| [**Win32 \_ POTSModemToSerialPort**](win32-potsmodemtoserialport.md) | 將數據機和數據機使用的序列埠相關聯。<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>影片和監視類別

影片和監視子類別會將代表監視器、視訊卡及其相關設定的類別分組。



| 類別                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | 代表連接到電腦系統的監視或顯示裝置類型。<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | 代表執行 Windows 之電腦系統的視訊卡設定資訊。 這個類別已經過時。 若要取代這個類別，請使用 [**win32 \_ VideoController**](win32-videocontroller.md)、 [**win32 \_ DesktopMonitor**](win32-desktopmonitor.md)和 [CIM \_ VideoControllerResolution](cim-videocontrollerresolution.md) 類別中的屬性。<br/> |
| [**Win32 \_ VideoController**](win32-videocontroller.md)                               | 表示在執行 Windows 的電腦系統上，視訊控制器的功能和管理能力。<br/>                                                                                                                                                                                                                                                       |
| [**Win32 \_ VideoSettings**](win32-videosettings.md)                                   | 將可套用的影片控制器和影片設定建立關聯。<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Win32 類別](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

