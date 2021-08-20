---
description: 本指南以 Microsoft Windows 的應用程式，找出效能受損的應用程式。
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: 辨識緩慢的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775239b76cfd287a446596f9a4a0eda6298caab35c31f70fade378ec0d44d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111812"
---
# <a name="recognizing-slow-applications"></a>辨識緩慢的應用程式

本指南以 Microsoft Windows 的應用程式，*找出效能受損的應用程式*。 緩慢的應用程式會展示下列一或多個徵兆：

-   CPU 和網路使用率偏低。

    電腦似乎正在等待一些東西。 通常，應用程式會在網路上等候。

-   透過 TCP \_ NODELAY 通訊端選項關閉 Nagle 演算法可提高效能。

    這表示其他問題，且不應視為解決方案。 關閉 Nagle 演算法會增加通訊協定額外負荷。 請勿使用這個方法來修正中斷的應用程式，只是表示應用程式需要其他工作來修正效能問題。

-   應用程式展現高負荷。

    若要計算您的應用程式額外負荷，請判斷您想要在每個方向傳輸多少資料。 然後，針對每個連線使用 Netstat，並為每個封包和500位元組新增 Ethernet 的 () 60 個位元組。 透過乙太網路進行串流處理所預期的最大負擔大約是6%。 針對數據機連線，最大的負擔大約是2%，因為 PPP 連結使用標頭壓縮。 如需詳細資訊，請參閱 [使用 Netstat 計算額外負荷](calculating-overhead-with-netstat-2.md) 。

-   當連接的 RTT 很大時，應用程式回應會變慢。

    假設應用程式未接近連結的頻寬，則大型 RTT 應該很少或沒有任何作用。 大型 RTT 的明顯減緩是序列化處理和許多小型交易的明確符號。

每個應用程式都應該在具有大型 RTT 的環境中進行測試。 這麼做會顯示從不佳的開發選項中遭遇的大部分應用程式。 這項測試可以在數種環境下執行，包括無線區域網路網路、連結延遲模擬器或衛星網路。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式行為](application-behavior-2.md)
</dt> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle 演算法](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



