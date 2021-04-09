---
title: 精簡布建邏輯單元
description: 精簡布建邏輯單元
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024231"
---
# <a name="thin-provisioning-of-logical-units"></a>精簡布建邏輯單元

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

Windows 精簡布建是端對端儲存體布建解決方案的介面。 若要提供高可用性、可擴充且方便使用的儲存體布建服務，您需要從伺服器主機到儲存體目標裝置的健全實行。 Windows 精簡布建功能可透過精簡布建邏輯單元的 (LUN 的) 識別、閾值通知、資源耗盡處理、空間回收，以及邏輯區塊定址 (LBA) 狀態抓取，來為系統管理員、IT 管理員和存放裝置系統管理員提供精簡布建存放裝置的同步觀點。 Windows 精簡布建功能提供穩固的儲存體布建服務模型，可套用至用戶端伺服器儲存體系統、虛擬化儲存體和雲端儲存體服務。 Microsoft 會強制執行存放裝置陣列產品的 Windows 精簡布建硬體認證套件需求，以確保高品質的精簡布建功能。

Windows 精簡布建儲存體解決方案：

-   允許存放裝置系統管理員以較少的實體磁片資源建立較大的 LUN
-   在不中斷儲存體布建服務的情況下新增或移除實體磁片資源
-   透過閾值設定將使用者的儲存體磁片區使用量警示
-   透過共用存放集區設定支援存放裝置布建
-   根據儲存空間的需求和使用量，增加或減少儲存集區的大小

Windows 精簡布建功能的摘要：

-   精簡布建 LUN 識別
-   閾值通知、暫存資源耗盡和永久資源耗盡的控制碼
-   儲存空間回收
-   邏輯區塊的對應狀態查詢

## <a name="manifestation"></a>表現

如果沒有適當瞭解精簡布建 LUN 的 Windows 控制碼，應用程式可能會因為未預期的行為或不明的原因而失敗。

## <a name="using-thin-provisioning-luns"></a>使用精簡布建 Lun

若要在 Windows 8 或 Windows Server 2012 中使用精簡布建的 Lun，系統和存放裝置系統管理員應留意這些重要事項：

-   精簡布建 LUN 識別;系統管理員或終端使用者可以使用重組和儲存優化器公用程式來識別存放裝置的媒體類型
-   當達到閾值或永久資源耗盡事件時，Windows 會記錄系統事件以警示系統管理員
-   儲存體空間回收可透過檔案刪除通知或存放裝置優化器的排程器來手動或自動執行
-   存放裝置系統管理員應執行閾值通知，以警示系統管理員或使用者，並避免任何未預期的儲存體服務中斷

## <a name="tests"></a>測試

-   存放裝置陣列必須接收 Windows 8 精簡布建憑證，才能支援 Windows 精簡布建功能
-   適用于存放裝置陣列的 Windows 精簡布建硬體認證套件將是一個有用的測試控管，可確認存放裝置陣列的 Windows 精簡布建功能支援的功能
-   Windows 預期精簡布建 LUN 和完整布建 LUN 可在相同的系統中運作，而不會發生任何問題

## <a name="resources"></a>資源

-   [T10 SCSI Block 命令規格 (SBC3r27) ](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [硬體儀表板服務](/windows-hardware/drivers/dashboard/)

 

 