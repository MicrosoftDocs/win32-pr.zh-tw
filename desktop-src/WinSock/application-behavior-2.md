---
description: 要考慮的應用程式開發的另一個層面是本機或 intracomputer 作業之間的行為差異，以及在兩部網路電腦之間進行作業時的行為。
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: 應用程式行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb09441eda4f0d909652ac38a9ca0596a1b4bce456f58c0e1eae1a7af7dc53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121458"
---
# <a name="application-behavior"></a>應用程式行為

要考慮的應用程式開發的另一個層面是本機或 intracomputer 作業之間的行為差異，以及在兩部網路電腦之間進行作業時的行為。 有些應用程式行為在本機電腦上的可接受很好，但是在網路上執行時，會造成顯著的效能降低和資源耗用量。 開發 Windows 通訊端應用程式時，應避免下列應用程式行為。

## <a name="behaviors-to-avoid"></a>要避免的行為

-   多對話應用程式。

    有些應用程式會執行許多小型交易。 結合與每個這類交易相關聯的網路額外負荷時，會將效果相乘。 在網路中，小型交易可耗用的資源數量和大型交易的時間很多。 更好的方法是將許多小型交易合併成單一大型交易。

-   序列化的交易。

    非必要的交易序列化可能會導致效能不佳，而且會影響擴充性。 例如，1000序列化交易至少需要 1000 \* RTT 才能完成。 更好的方法是以平行方式執行不相關的交易。 當序列化的應用程式與多對話應用程式結合時，回應可能會嚴重妨礙。

    > [!Note]  
    > 將應用程式正確還原序列化可能很困難。 如果從序列化變更為平行證明太困難，請考慮將多個交易結合為較少的大型交易。

     

-   Fat 交易。

    在網路上傳送不必要位元組的應用程式會被視為 fat 應用程式。 在網路上傳送不必要位元組的應用程式會增加網路額外負荷，而且會妨礙效能。 這種情況通常來自無效率的資料結構或無效率的資料串流。 若要解決此情況，請將資料結構優化，或考慮使用壓縮。

下列各節將討論要考慮的應用程式開發層面。

-   [TCP/IP 特定問題](tcp-ip-specific-issues-2.md)
-   [辨識緩慢的應用程式](recognizing-slow-applications-2.md)
-   [使用 Netstat 計算額外負荷](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



