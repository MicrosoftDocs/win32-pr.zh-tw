---
description: Microsoft Hyper-V server 提供可調整、可靠且高可用性的虛擬機器管理環境。 Hyper-v 虛擬機器軟體會合並伺服器和開發與測試環境。
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: 'Hyper-v WMI 提供者 (V2) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555fd3cd1e8420c59bb5f1b8ef16480b3ddfcf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973447"
---
# <a name="hyper-v-wmi-provider-v2"></a>Hyper-v WMI 提供者 (V2) 

## <a name="purpose"></a>目的

Hyper-v 提供可調整、可靠且高度可用的虛擬化伺服器運算環境。 它可讓一或多個客體作業系統同時在單一實體電腦上執行。 虛擬機器技術的主要用途包括下列各項：

-   伺服器合併
-   合併開發與測試環境
-   簡化嚴重損壞修復

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                 | 描述                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 Hyper-v WMI 提供者](about-the-virtualization-wmi-provider.md)<br/>                | Hyper-v 的 WMI 提供者可讓開發人員和腳本撰寫人員快速建立虛擬化平臺的自訂工具、公用程式和增強功能。 WMI 介面可以管理 Hyper-v 服務的所有層面。<br/> |
| [使用 Hyper-v WMI 提供者](using-the-virtualization-wmi-provider.md)<br/>                | 下列主題說明如何使用 Hyper-v WMI 提供者。<br/>                                                                                                                                                            |
| [Hyper-v WMI 類別](hyper-v-wmi-classes.md)<br/>                                             | 以下是 Hyper-v WMI 類別。<br/>                                                                                                                                                                                    |
| [Hyper-v 應用程式健康情況監視 API](hyper-v-application-health-monitoring-api.md)<br/> | Hyper-v 應用程式健康情況監視 API 可用來監視虛擬機器中執行之應用程式的健全狀況狀態。<br/>                                                                                               |
| [Hyper-v 複寫 API](hyper-v-replication-api.md)<br/>                                     | Hyper-v 複寫 API 用來控制虛擬機器複寫和容錯移轉復原。<br/>                                                                                                                             |
| [Hyper-v 計量 API](hyper-v-metrics-api.md)<br/>                                             | Hyper-v 計量 API 可用來監視虛擬機器中執行之應用程式的健全狀況狀態。<br/>                                                                                                                     |
| [Hyper-v 網路 API](hyper-v-networking-api.md)<br/>                                       | Hyper-v 網路 API 是用來控制 Hyper-v 中的網路功能。<br/>                                                                                                                                                          |
| [Hyper-v 遷移 API](hyper-v-storage-migration-api.md)<br/>                                 | Hyper-v 遷移 API 是用來控制 Hyper-v 的儲存和即時移轉。<br/>                                                                                                                                           |
| [Hyper-v 虛擬光纖通道 API](hyper-v-virtual-fiber-channels-api.md)<br/>                | Hyper-v 虛擬光纖通道 API 是用來控制 Hyper-v 中的虛擬光纖通道介面卡。<br/>                                                                                                                           |
| [Hyper-v VM 放置 API](hyper-v-vm-placement-api.md)<br/>                                   | Hyper-v 虛擬機器 (VM) 放置 API 包含 Vm 或主控電腦系統的相容性資訊。<br/>                                                                                                        |
| [閾值類別](threshold-classes.md)<br/>                                                 | 包含 Windows 10 中引進的類別。<br/>                                                                                                                                                                                |
| [RS2 類別](redstone-classes.md)<br/>                                                        | 包含 Windows 10 1703 版的新類別。<br/>                                                                                                                                                                        |
| [RS3 類別](rs3-classes.md)<br/>                                                             | 包含 Windows 10 1709 版的新類別。<br/>                                                                                                                                                                        |
| [Hyper-v 詞彙](virtualization-glossary.md)<br/>                                            | Windows 虛擬化 SDK 檔中使用的詞彙。<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>執行階段需求求

Hyper-v 服務需要支援執行 Hyper-v 硬體輔助虛擬化的 x64 型系統。 不過，與 Hyper-v WMI 介面互動的程式可以在任何支援 WMI 的系統上遠端執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Hyper-v (Windows Server 2008 R2 技術文件庫) ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Server Virtualization](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

