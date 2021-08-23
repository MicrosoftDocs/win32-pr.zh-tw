---
description: 公開機器檢查架構 (MCA) 的一組 WMI 類別。 系統抽象層 (SAL) 提供 MSMCA 類別中報告的所有事件。 Intel Corporation 開發和擁有 MCA。
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: MSMCA 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0f70bead9acbbb23fe0e2115ac12f967c7908f1f0eefa16d65cd1a57947e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641078"
---
# <a name="msmca-classes"></a>MSMCA 類別

Microsoft 機器檢查架構 (MSMCA) 類別是一組 WMI 類別，可公開機器檢查架構 (MCA) 。 系統抽象層 (SAL) 提供 MSMCA 類別中報告的所有事件。 Intel Corporation 開發和擁有 MCA。



| 類別                                                                               | 描述                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | 代表 CPU 錯誤事件。                                                                          |
| [**MSMCAEvent \_ 標頭**](msmcaevent-header.md)                                     | 代表所有 MSMCAEvent 類別使用的一般標頭。                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | 代表 (MCA) 無效錯誤的記憶體檢查架構。                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | 表示 MCA 記憶體錯誤事件。                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | 指出作業系統已移除實體頁面的記憶體。                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | 表示 MCA PCI 匯流排錯誤。                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | 表示 MCA PCI 元件錯誤。                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | 表示 MCA 平臺特定的錯誤。                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | 表示 MCA 系統 bios 錯誤。                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | 指出已將已更正的機器檢查處理切換為輪詢。                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | 表示 MCA 系統事件錯誤。                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | 從中衍生所有機器檢查架構 (MCA) 提供者資料類別的抽象基類。 |
| [**MSMCAInfo \_ 專案**](msmcainfo-entry.md)                                         | 表示 MCA、已更正的機器檢查 (CMC) ，或更正的平臺錯誤 (CPE) 資訊專案。 |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | 包含 CMC 事件。                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | 包含已更正的平臺事件。                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | 指定原始 MCA 記錄。                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | 包含 MCA 事件。                                                                                  |
| [**>register-wmievent**](wmievent.md)                                                        | 衍生所有 MCA 提供者事件類別的來源抽象基類。                             |



 

 

 



