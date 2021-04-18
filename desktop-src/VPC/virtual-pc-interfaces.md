---
title: Windows Virtual PC 介面
description: Windows Virtual PC 支援下列介面。
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC，介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965236"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Virtual PC 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

Windows Virtual PC 支援下列介面。



| 介面                                                                             | 描述                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | 提供虛擬機器 (VM) 的帳戶計量相關資訊的存取權。<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | 控制 VM 的顯示設定。<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | 控制 VM 內的 CD-ROM 或 DVD-ROM 光碟機。<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | 定義 VM 中的 CD 和 DVD 光碟機集合。<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | 定義 [**IVMDVDDrive**](ivmdvddrive.md) 介面的外寄事件介面。<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | 控制 VM 內的軟碟磁碟機。<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | 定義 VM 內的磁片磁碟機集合。<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | 定義 [**IVMFloppyDrive**](ivmfloppydrive.md) 介面的外寄事件介面。<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | 定義在 VM 內執行的客體作業系統。<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | 提供硬碟影像的存取。<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | 定義 VM 內硬碟的連接。<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | 定義 VM 內的硬碟連接集合。<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | 抓取主機電腦的相關資訊。<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | 控制 VM 內的鍵盤裝置。<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | 控制 VM 內的滑鼠裝置。<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | 作為虛擬網路介面卡的介面， (NIC 內的 NIC) 。<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | 定義虛擬 Nic 在 VM 內的集合。<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | 定義 VM 內的平行埠。<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | 定義 VM 內的平行埠集合。<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | 定義 VM 內的序列埠。<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | 定義 VM 內序列埠的集合。<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | 用來監視和控制各種方法的非同步工作。<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | 定義 VM 中工作物件的集合。<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | 定義連接至主機系統的 USB 裝置介面。<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | 定義連接至主機系統的 USB 裝置集合。<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | 定義 VM 的介面。<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | 定義 Windows Virtual PC 中的 Vm 集合。<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | 定義 [**IVMVirtualMachine**](ivmvirtualmachine.md) 介面的外寄事件介面。<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | 定義虛擬網路。<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | 定義 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件的集合。<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | 定義最上層的 Windows Virtual PC 應用程式物件。<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | 定義 [**IVMVirtualPC**](ivmvirtualpc.md) 介面的外寄事件介面。<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>適用于64位 Windows 的開發人員注意事項

在64位版本的 Windows 上，Windows Virtual PC 的類型程式庫位於% WinDir% System32 目錄中的64位二進位 (VPC.exe) \\ 。 預設不會顯示該目錄到32位進程;WOW64 預設會將% WinDir% System32 目錄的所有存取對應 \\ 至% windir% \\ SysWOW64 目錄。 Visual Studio 是32位的二進位檔案，因此無法在此位置開啟檔案。 若要產生 Windows Virtual PC 的互通性元件，請使用 Visual Studio 和 Windows SDK 隨附的 TlbImp.exe。 若要產生 *Microsoft.VirtualPC.Interop.dll*，請使用下列命令列：

**TlbImp.exe/out： * * * Microsoft.VirtualPC.Interop.dll* **/namespace： Microsoft. VirtualPC. Interop% WinDir% \\ System32 \\VPC.exe**

其他方案包括將 VPC.exe 複製到不同的目錄，讓編譯器可以找到它，或使用 Windows SDK 中的 OleView.exe 工具，從 VPC.exe 的類型程式庫中解壓縮 .idl 檔。

 

