---
description: Microsoft Windows 網路元件已針對效能和擴充性而開發。
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: 高效能 Windows 通訊端應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df2b050ac45bf0bf7788a356f4fdba98197d481dd99180f99f7dbf8cdfb5b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927867"
---
# <a name="high-performance-windows-sockets-applications"></a>高效能 Windows 通訊端應用程式

Microsoft Windows 網路元件已針對效能和擴充性而開發。 這可讓應用程式將可用的網路頻寬最大化。 Windows通訊端和 Windows tcp/ip 通訊協定堆疊已經過微調和簡化。 如此一來，正確撰寫 Windows 的應用程式可達到異常的輸送量和效能，如下列事實所示：

-   Windows 能夠提供超過200000的同時 TCP 連線。
-   在 SPECWeb96 所進行的測試中，Windows 上的 Internet information Server 每秒提供超過25000的 HTTP 要求。
-   Windows 在包含10個躍點的跨洲 gigabit 網路上設定超過750Mbps 的傳輸記錄。

這些成就說明 Windows tcp/ip 處理資料的速度非常快。 但是，許多應用程式都不會利用 Windows、tcp/ip 和 Windows 通訊端效能功能，因為它們會不知不覺地實行效能阻礙技術。

在本指南中，您將瞭解如何找出常見的程式設計錯誤，以及如何避免這些錯誤。 然後，您將學習可讓 Windows 通訊端應用程式能以最佳方式執行的技術。 本指南會在六個章節中提供。 區段的順序是刻意的;若要充分利用本指南，請依序閱讀。 下表提供每個區段的連結，以及每個主題的簡短描述。



| 主題                                                                                            | 描述                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [網路術語](network-terminology-2.md)                                                 | 定義瞭解網路應用程式效能所需的網路術語和計量。                                     |
| [效能維度](performance-dimensions-2.md)                                           | 討論影響應用程式的認知和實際網路效能的效能維度。                                        |
| [TCP/IP 特性](tcp-ip-characteristics-2.md)                                           | 定義可能導致寫入不良應用程式效能問題的 TCP/IP 通訊協定特性。                                     |
| [應用程式行為](application-behavior-2.md)                                               | 說明如何辨識效能不良之網路應用程式的徵兆。                                                                     |
| [改善應用程式緩慢](improving-a-slow-application-2.md)                               | 提供應用程式設計問題的範例，這些問題會對效能不佳的應用程式造成影響，並變更程式碼以改善效能。 |
| [互動式應用程式的最佳作法](best-practices-for-interactive-applications-2.md) | 列出開發最佳互動式網路應用程式所採用的最佳做法。                                                         |



 

 

 



