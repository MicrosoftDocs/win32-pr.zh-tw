---
description: 下列清單包含 TAPI MSP 設計目標。
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: 一般設計目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972451"
---
# <a name="general-design-goals"></a>一般設計目標

下列清單包含 TAPI MSP 設計目標。

-   基類已保持簡單，只有在絕對必要時才會引進成員和方法。
-   簡單的繼承。 類別之間不會有多重繼承，不過介面會使用多個繼承。
-   鎖定只會在一個方向進行，以防止鎖死。 呼叫物件上需要鎖定呼叫的方法，可能會在資料流程上呼叫需要鎖定的方法。 不過，資料流程上需要鎖定的方法永遠不會呼叫呼叫上需要鎖定的方法。
-   Refcounts 可用來保護存取。 所有張貼到執行緒集區的回呼都有 refcounts。 Refcount 會在等候取消時取消。 位址物件在終端機上有 refcounts。 呼叫物件具有位址和資料流程上的 refcounts。 資料流程物件具有呼叫和終端機的 refcounts。 終端機已 refcounts 資料流程。 呼叫位址和呼叫物件的 shutdown 方法時，迴圈 refcounts 中斷。

 

 



