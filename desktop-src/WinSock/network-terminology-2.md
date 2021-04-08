---
description: 計量可用來測量網路和通訊協定效能的各個層面。
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: " (Windows 通訊端 2) 的網路術語"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690387"
---
# <a name="network-terminology-windows-sockets-2"></a> (Windows 通訊端 2) 的網路術語

計量可用來測量網路和通訊協定效能的各個層面。 在各種案例中，這類計量的值會指出網路應用程式的效能層級。 本章節定義了業界廣泛用來測量網路應用程式效能的詞彙和計量。 本指南的其餘部分會使用這些詞彙。

-   來回行程時間 (RTT) 

    從來源電腦到目的地電腦的往返要求的時間（以毫秒為單位），然後重新執行。 較低的值表示效能較佳。 轉寄和傳回路徑時間不一定相等。

    RTT 值會受到網路基礎結構、節點與網路條件之間的距離，以及封包大小的影響。 當針對低速連結（例如撥號連線）測量時，封包大小、擁塞和承載 compressibility 會影響 RTT。 其他因素會影響 RTT，包括轉寄錯誤修正和資料壓縮，這會導入增加 RTT 的緩衝區和佇列，因此會降低效能。

-   Goodput

    接收者成功處理的實用應用程式資料量（以每秒位數為單位）。 Goodput 可測量有效或實用的輸送量，並只包含應用程式資料;封包、通訊協定和媒體標頭會被視為額外負荷，而且不是 goodput 的一部分。

-   通訊協定額外負荷

    Nonapplication 的位元組，包括通訊協定和媒體框架，除以傳輸的位元組總數。 此值以百分比表示。 較高的值表示效能較差。

    本指南中的雙向會計算出額外負荷，但可以個別計算每個方向的費用。

-   Bandwidth-Delay 產品

    網路的每秒每秒頻寬的乘積，而 RTT (以秒為單位) 。 此值等於填滿可用的網路頻寬所花費的位數。 當頻寬延遲產品的值偏高時，TCP/IP 堆疊必須處理大量未認可的資料，才能讓管線保持完整。 頻寬延遲產品是串流應用程式的關鍵端對端計量。

 

 



