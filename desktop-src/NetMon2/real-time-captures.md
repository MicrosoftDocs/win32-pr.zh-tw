---
description: 監視器會以即時模式接收已捕捉的網路畫面。 網路封包提供者會使用 IRTC COM 介面的提供者來捕捉框架 (NPP) ，然後在其中一個監視中將兩個執行執行緒的監視器傳遞給監視器。
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Real-Time 的捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852916"
---
# <a name="real-time-captures"></a>Real-Time 的捕獲

監視器會以即時模式接收已捕捉的網路畫面。 [*網路封包提供者*](n.md)會使用提供者的 [IRTC](irtc.md) COM 介面 (NPP) 來捕捉框架，然後將這些框架傳遞給其中一個監視的兩個執行執行緒中的監視器。

監視器可將 [*捕獲篩選器*](c.md) 傳遞至提供框架的 NPP，以限制它們必須處理的畫面格數目。 一般而言，特定監視是設計來監看特定類型的流量，例如 HTTP、RIPX 或 SMB。 不同于使用精密剖析器來選取要分析之資訊的專家，監視器必須檢查每個框架是否有設計偵測的條件。 這個框架框架的方法背後的原因是效能。 監視器必須快速處理其框架，使其不會落在驅動程式後方，以提供 NPP 的畫面。 否則，資料將會遺失。

 

 



