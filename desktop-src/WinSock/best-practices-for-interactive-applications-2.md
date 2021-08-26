---
description: 在變形生命資料格更新程式碼時，已發現數個撰寫高效能網路應用程式的指導方針。
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: 互動式應用程式的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497fc56419f8859b7490671590b4589092c4c5b37047a01b0bf80cee9bf8c213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996898"
---
# <a name="best-practices-for-interactive-applications"></a>互動式應用程式的最佳作法

在變形生命資料格更新程式碼時，已發現數個撰寫高效能網路應用程式的指導方針。 撰寫這些類型的應用程式時適用的一些一般策略如下：

-   盡可能讓資料流程，而不是傳入區塊。
-   使用一些大型交易，而不是許多小型交易。 大型交易也可以有效率地進行資料流程處理。
-   辨識網路是很慢且不可靠的資源，並開發每個應用程式，以將其對網路的依賴降至最低。
-   在網路上使用架構良好的資料標記法。 資料標記法應該是電腦架構中立、不包含 fat，而且可能會壓縮。
-   在初始化和關閉期間，請不要讓使用者等待網路啟動或關閉。 網路相關的初始化可能需要相當長的時間。 分隔非關鍵性的網路程式碼。
-   適當地處理其影響的錯誤。 並非所有的錯誤都很重要。 執行復原機制並提供不造成干擾的使用者意見反應。
-   只有在適當時，才 (RPC) 使用遠端程序呼叫。 RPC 在 Windows Me/98 上是同步的，而且在用來傳送少量資料的情況下，一律會產生多對話、fat 的通訊協定。
-   使用 Netstat 測量您的網路額外負荷;您可能會對度量所顯示的內容感到驚訝。
-   在各式各樣的網路上測試應用程式，尤其是緩慢或易失的網路。 無線區域網路網路、數據機和虛擬私人網路 (VPN) 在網際網路上，是很好的網路來進行測試。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



