---
description: 串流執行緒和篩選圖形管理員
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: 串流執行緒和篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978241"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>串流執行緒和篩選圖形管理員

當篩選圖形管理員停止圖形時，會等候所有串流執行緒關閉。 這對篩選準則具有下列含意：

-   篩選絕不能從資料流程執行緒呼叫篩選圖形管理員上的方法。

    篩選圖形管理員會使用重要區段來同步處理自己的作業。 如果串流執行緒嘗試保存此重要區段，它可能會造成鎖死。 例如：假設另一個執行緒停止圖形。 該執行緒會採用篩選圖形鎖定，並等候篩選停止傳遞資料。 如果您的篩選器正在等候鎖定，則永遠不會停止，因而造成鎖死。

-   篩選絕不能從串流執行緒 **AddRef** 或 **QueryInterface** 篩選圖形管理員。

    如果篩選 (透過 **AddRef** 或 **QueryInterface**) 在篩選圖形管理員上保存參考計數，它可能會成為保存參考計數的最後一個物件。 當篩選呼叫 **釋放** 時，篩選圖形管理員會終結本身。 在其清除常式內，篩選圖形管理員會嘗試停止圖形，使其等候串流執行緒結束。 但是，它正在串流執行緒內等候，所以串流執行緒無法結束。 結果是鎖死。

 

 



