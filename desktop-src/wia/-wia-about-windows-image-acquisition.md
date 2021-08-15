---
description: Windows 影像取得 (WIA) 介面都是 API 和設備磁碟機介面 (DDI) 。
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: 關於取得 Windows 映像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451298"
---
# <a name="about-windows-image-acquisition"></a>關於取得 Windows 映像

Windows 影像取得 (WIA) 介面都是 API 和設備磁碟機介面 (DDI) 。 WIA API 的設計目的是要讓應用程式能夠：

-   在穩固且穩定的環境中執行。
-   將互通性問題降至最低。
-   列舉可用的映射取得裝置。
-   同時建立多個裝置的連接。
-   以標準且可擴充的方式查詢裝置屬性。
-   使用標準和高效能傳輸機制來取得裝置資料。
-   維護資料傳輸之間的影像屬性。
-   收到各種裝置事件的通知。

WIADDI 的設計目的是要將硬體廠商必須撰寫的程式碼數量降到最低，同時維持製作個別解決方案的彈性。 這可透過下列方式完成：

-   提供可執行大部分驅動程式作業的標準裝置服務程式庫。
-   提升產業裝置通訊標準，讓一個 WIA 驅動程式支援大部分的 WIA 裝置。 例如，圖片傳輸通訊協定 (PTP) 。
-   允許設備磁碟機支援自訂介面，而不需要使用標準裝置服務程式庫。 不過，驅動程式仍然需要執行標準的 WIA 介面。

本節提供下欄區域中的 WIA 介面簡短總覽：

-   [WIA 架構](-wia-wia-architecture.md)
-   [STI 相容性](-wia-sti-compatibility.md)
-   [TWAIN 相容性](-wia-twain-compatibility.md)
-   [WIA 裝置管理員](-wia-wia-device-manager.md)
-   [WIA 迷你驅動程式服務程式庫](-wia-wia-minidriver-service-library.md)
-   [WIA 迷你驅動程式](-wia-wia-minidriver.md)

 

 



