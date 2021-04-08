---
title: 偵測和避免複寫延遲
description: 複寫延遲是在鬆散結合的分散式系統中的生活事實。
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671347"
---
# <a name="detecting-and-avoiding-replication-latency"></a>偵測和避免複寫延遲

複寫延遲是在鬆散結合的分散式系統中的生活事實。 應用程式必須配合此。 解決複寫延遲的最佳方式，是設計應用程式以將效果降到最低。 理想的啟用目錄應用程式：

-   不區分版本扭曲。
-   不相依于多個物件之間的關聯性。
-   沒有內部或物件間的一致性需求。

符合此設定檔的應用程式和服務不需要考慮複寫延遲。 其他應用程式必須以複寫延遲為考慮而設計。 設計這類應用程式成功的關鍵在於複寫程式的認知。 在設計階段用來減少物件間相依性，並將部分更新視窗降至最低的步驟，會在執行時間支付龐大的紅利。 處理複寫延遲的方法分為兩個類別，也就是避免延遲和偵測策略影響的策略，可讓應用程式偵測延遲引發的狀態。

 

 




