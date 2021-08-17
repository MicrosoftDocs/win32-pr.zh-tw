---
description: 虛擬磁碟服務 (VDS) 管理各種不同的存放裝置設定，從單一磁片桌面到外部存放裝置陣列。 此服務會公開應用程式設計介面， (API) 。
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: 虛擬磁碟服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137131"
---
# <a name="virtual-disk-service"></a>虛擬磁碟服務

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代虛擬磁碟服務 COM 介面。\]

## <a name="purpose"></a>目的

虛擬磁碟服務 (VDS) 管理各種不同的存放裝置設定，從單一磁片桌面到外部存放裝置陣列。 此服務會公開應用程式設計介面， (API) 。

## <a name="where-applicable"></a>適用時

從 Windows 8 和 Windows Server 8 開始，虛擬磁碟服務 COM 介面會由儲存體管理 API （以 WMI 為基礎的程式設計介面）取代。 若要管理儲存子系統、 (Windows) 磁片、磁碟分割和磁片區，強烈建議使用儲存體管理 API。 如需詳細資訊，請參閱[Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)。

針對鏡像開機磁碟區以外的所有使用方式 (使用鏡像磁片區來裝載作業系統 ) ，動態磁碟已淘汰。 對於需要復原磁片磁碟機失敗的資料，請使用儲存空間，這是一個彈性的儲存體虛擬化解決方案。 如需詳細資訊，請參閱[儲存空間 Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))。

使用本指南中所述介面的應用程式開發人員可以查詢及設定一組異類廠商提供和內部受控儲存體。 VDS 會從應用程式中隱藏與儲存體相關的複雜性，讓服務與廠商和技術中立。

## <a name="developer-audience"></a>開發人員對象

本檔適用于熟悉 Microsoft Windows 平臺的儲存功能，以及瞭解 COM 開發的應用程式開發人員。

本指南也適用于開發和支援 VDS 硬體提供者計畫的硬體子系統製造商。

## <a name="run-time-requirements"></a>執行階段需求求

Windows Server 2003、Windows Vista 和更新版本都支援 VDS。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素檔集的需求一節。

支援在 WOW64 下執行32位 vds 應用程式，但64位 vds 提供者必須以原生應用程式的形式在64位 Windows 版本上執行。

Microsoft Windows 軟體開發套件 (SDK) 提供 VDS。 您可以從[Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)安裝適用于 Windows 7 和 Windows Server 2008 R2 的 SDK。 這一版的 Windows SDK 可以用來開發適用于 Windows Server 2003、Windows Vista 和更新版本的 VDS 應用程式。 您也可以從 Windows 下載中心下載 SDK 的[ISO 版本](https://www.microsoft.com/download/details.aspx?id=8442)。

## <a name="in-this-section"></a>本節內容



| 主題                                         | 描述                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [關於 VDS](about-vds.md)<br/>         | 描述 VDS 物件模型、存放裝置設定策略和 VDS 通知。<br/>    |
| [使用 VDS](using-vds.md)<br/>         | 說明如何使用 VDS 來查詢和設定存放裝置。<br/>                            |
| [VDS 參考](vds-reference.md)<br/> | 描述 VDS 常數、資料類型、列舉、介面、結構和錯誤碼。<br/> |



 

 

