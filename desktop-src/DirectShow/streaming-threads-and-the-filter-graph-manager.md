---
description: 串流處理執行緒和篩選 Graph 管理員
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: 串流處理執行緒和篩選 Graph 管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329768"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>串流處理執行緒和篩選 Graph 管理員

當篩選 Graph 管理員停止圖形時，會等待所有串流執行緒關閉。 這對篩選準則具有下列含意：

-   篩選準則永遠不能從串流執行緒 Graph 管理員呼叫篩選器上的方法。

    篩選 Graph 管理員會使用重要區段來同步處理自己的作業。 如果串流執行緒嘗試保存此重要區段，它可能會造成鎖死。 例如：假設另一個執行緒停止圖形。 該執行緒會採用篩選圖形鎖定，並等候篩選停止傳遞資料。 如果您的篩選器正在等候鎖定，則永遠不會停止，因而造成鎖死。

-   篩選絕不能從串流執行緒 Graph 管理員 **AddRef** 或 **QueryInterface** 篩選篩選。

    如果篩選 Graph 管理員 (透過 **AddRef** 或 **QueryInterface**) 來保存參考計數，它可能會成為保存參考計數的最後一個物件。 當篩選準則呼叫 **Release** 時，篩選 Graph 管理員會終結本身。 在其清除常式內，篩選 Graph 管理員會嘗試停止圖形，使其等候串流執行緒結束。 但是，它正在串流執行緒內等候，所以串流執行緒無法結束。 結果是鎖死。

 

 



