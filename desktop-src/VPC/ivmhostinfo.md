---
title: 'IVMHostInfo 介面 (VPCCOMInterfaces .h) '
description: 抓取主機電腦的相關資訊。 IVMVirtualPC HostInfo 屬性會傳回 IVMHostInfo 物件。
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- IVMHostInfo 介面 Virtual PC
- IVMHostInfo 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ca5f296dd4a7437ea136dbaee0d04c68a93efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094543"
---
# <a name="ivmhostinfo-interface"></a>IVMHostInfo 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取主機電腦的相關資訊。 **IVMHostInfo** 物件會從 [**IVMVirtualPC：： HostInfo**](ivmvirtualpc-hostinfo.md)屬性傳回。

## <a name="members"></a>成員

**IVMHostInfo** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMHostInfo** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMHostInfo** 介面具有這些屬性。



| 屬性                                                                                  | 存取類型          | Description                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | 唯讀<br/> | 與主機 CD 和 DVD 裝置相關聯的磁碟機號。<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | 唯讀<br/> | 與主機軟碟磁碟機相關聯的磁碟機號。<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | 唯讀<br/> | 主機電腦中的邏輯處理器數目。<br/>                                   |
| [**記憶**](ivmhostinfo-memory.md)<br/>                                           | 唯讀<br/> | 主機電腦中的實體記憶體總數量（以 mb 為單位）。<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | 唯讀<br/> | 主機電腦可用的實體記憶體數量（以 mb 為單位）。<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | 唯讀<br/> | 主機電腦中可用的實體記憶體數量（以 mb 為單位），表示為字串。<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | 唯讀<br/> | 主機電腦中的實體記憶體總數量（以 mb 為單位），表示為字串。<br/>     |
| [**Mmx**](ivmhostinfo-mmx.md)<br/>                                                 | 唯讀<br/> | 指出處理器是否支援 MMX 指令集。<br/>                       |
| [**NetworkAdapters**](ivmhostinfo-networkadapters.md)<br/>                         | 唯讀<br/> | 主機電腦中的可列舉 Nic 集合。<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | 唯讀<br/> | 主機電腦中 TCP/IP 位址的可列舉集合。<br/>                       |
| [**OperatingSystem**](ivmhostinfo-operatingsystem.md)<br/>                         | 唯讀<br/> | 在主機電腦上執行的作業系統。<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | 唯讀<br/> | 在主機電腦上執行之作業系統的主要版本。<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | 唯讀<br/> | 在主機電腦上執行之作業系統的次要版本。<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | 唯讀<br/> | 在主機電腦上執行之作業系統的 service pack 資訊。<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | 唯讀<br/> | 在主機電腦上執行的作業系統版本。<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | 唯讀<br/> | 可以附加至來賓的主機平行埠。<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | 唯讀<br/> | 主機電腦中的實體處理器數目。<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | 唯讀<br/> | 主機處理器所支援的功能清單。<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | 唯讀<br/> | 主機處理器的製造商。<br/>                                                 |
| [**>processorspeed**](ivmhostinfo-processorspeed.md)<br/>                           | 唯讀<br/> | 主機處理器的速度，以兆赫 (MHz)  (或 ghz) 。<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | 唯讀<br/> | 主機處理器的速度，以兆赫或 ghz 為字串。<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | 唯讀<br/> | 主機處理器的版本。<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | 唯讀<br/> | 與主機序列埠相關聯的序列埠名稱。<br/>                                |
| [**Sse**](ivmhostinfo-sse.md)<br/>                                                 | 唯讀<br/> | 指出處理器是否支援 SSE 指令集。<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | 唯讀<br/> | 指出處理器是否支援 SSE2 指令集。<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | 唯讀<br/> | 指出處理器是否支援3DNow 指令集。<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | 唯讀<br/> | 主機電腦上的 UTC 時間。<br/>                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



 

