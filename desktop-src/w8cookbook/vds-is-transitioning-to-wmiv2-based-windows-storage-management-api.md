---
title: 虛擬磁碟服務正在轉換至 Windows 儲存體管理 API
description: 虛擬磁碟服務正在轉換至 Windows 儲存體管理 API
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383037"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a>虛擬磁碟服務正在轉換至 Windows 儲存體管理 API

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

從 Windows 8 和 Windows Server 2012 開始，虛擬磁碟服務 COM 介面會由儲存體管理 API （以 WMI 為基礎的程式設計介面）取代。 若要管理儲存子系統、 (Windows) 磁片、磁碟分割和磁片區，強烈建議使用存放裝置管理 API。 如需詳細資訊，請參閱 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)。

針對鏡像開機磁碟區以外的所有使用方式 (使用鏡像磁片區來裝載作業系統) ，動態磁碟已淘汰。 對於需要針對磁片磁碟機失敗進行復原的資料，請使用儲存空間，這是一個彈性的儲存體虛擬化解決方案。 如需詳細資訊，請參閱 [儲存空間技術預覽](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))。

您可以在淘汰期間繼續使用 DiskPart、DiskRAID 和磁片管理，但是這些工具將無法搭配儲存空間使用，也不適用於任何其他新的 Windows Management Instrumentation (WMI) 架構的 Windows 儲存管理 Api 或內建的存放裝置管理公用程式或用戶端。


| API | 儲存子系統 | 基本磁碟 | 動態磁碟 | 儲存空間 |
| --- | --- | --- | --- | --- |
| Vds | 是 | 是 | 是 | 否 |
| WMI | 是 | 是 | 否 | 是 |
| DiskPart | n/a | 是 | 是 | 否 |
| DiskRAID |  是 | n/a | n/a | n/a |
| 磁片管理 GUI | n/a | 是 | 是 | 否 |
| PowerShell | 是 | 是 | 否 | 是 |
| 儲存空間主控台 | n/a | 否 | 否 | 是 |


這項轉換的結果將會提高儲存體復原能力、可用性和擴充性;統一的腳本和程式設計語言、降低存放裝置管理成本，以及更輕鬆的遠端存放裝置管理。

## <a name="manifestation"></a>表現

VDS 環境中使用的 DiskPart 和 DiskRAID 公用程式不支援新的儲存空間。 同樣地，新的儲存體 PowerShell 公用程式不支援已被取代的動態磁碟

## <a name="mitigation"></a>降低

Microsoft 強烈建議您將任何新的儲存體管理應用程式放在 Windows 儲存體管理 API，並規劃在標準更新週期期間，將以 VDS 基礎結構為基礎的現有應用程式轉換成 Windows 儲存體管理 API。

## <a name="resources"></a>資源

-   [Windows 儲存裝置管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [Windows PowerShell 中的儲存體 Cmdlet](/powershell/module/storage/?view=win10-ps)
-   [Windows Management Instrumentation](../wmisdk/wmi-start-page.md)
-   [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)

 

 