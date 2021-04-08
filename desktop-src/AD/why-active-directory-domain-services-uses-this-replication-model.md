---
title: 為何 Active Directory Domain Services 使用此複寫模型
description: 本主題說明 Active Directory Domain Services 用於複寫模型的自由格式系統的原因。
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- 複寫模型 Active Directory，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839256"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>為何 Active Directory Domain Services 使用此複寫模型

本主題說明 Active Directory Domain Services 用於複寫模型的自由格式系統的原因。

Active Directory Domain Services 是一個自由形式的系統，原因如下：

-   客戶需要高度分散的解決方案，其中的目錄部分可以散佈在其網路上，並在本機進行管理。
-   大型客戶通常會成長至數百萬個物件、數百個或數千個複本，或兩者。
-   許多客戶網路只提供與某些位置的間歇性連線;例如，遠端石油切入平臺並在海洋推出，因此系統必須能夠容忍部分連線或中斷連線的作業。

無法保證對分散式系統目前或未來狀態的完全感知，因為必須傳播狀態變更的知識，而且傳播需要一些時間，在這段期間可能會發生更多狀態變更。

緊密結合的系統會藉由嘗試消除不確定的方式來處理不確定性。 這是透過更新的限制所完成，要求所有節點或某些多數節點都可供使用，然後才可以執行更新、使用分散式鎖定配置或單一掌控的關鍵資源、限制所有節點的連接，或這些技巧的組合。 在分散式系統中，更緊密結合的運算節點是調整規模限制較低的位置。

自由形式的系統會藉由容許來處理不確定性。 自由形式的系統可讓節點擁有整體系統狀態的不同視圖，並提供演算法來解決衝突。

因為本機系統管理、中斷連線的作業，以及非常大量節點的擴充性需求，所以將緊密結合的解決方案拒絕為不適合 Active Directory Domain Services。 選擇的鬆散結合模型、聚合的多宿主鬆散一致性，滿足所有需求。

 

 




