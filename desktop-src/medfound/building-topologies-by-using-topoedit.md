---
description: 使用 TopoEdit 建立拓撲
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: 使用 TopoEdit 建立拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e678e0c25cbfe56c2633091820468a6c0313663847870a4de5c912a5edae95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959431"
---
# <a name="building-topologies-by-using-topoedit"></a>使用 TopoEdit 建立拓撲

拓撲必須具有下列三個節點：

-   來源節點：來自媒體檔案的資料流程，用來做為拓撲的來源。
-   轉換節點：媒體基礎轉換 (MFT) 。 這些節點通常是針對拓撲的編碼器、解碼器和效果。
-   輸出節點：將媒體資料、影片畫面或音訊串流傳遞給媒體會話以進行播放的資料流程接收。

如需拓撲結構的詳細資訊，請參閱 [關於](about-topologies.md)拓撲。

若要建立拓撲，您必須加入節點、連接節點，並解析拓撲，以便可以播放。

拓撲節點會顯示為方塊，顯示節點名稱的文字。 綠色方塊代表使用者新增的節點。 解決拓撲時，TopoEdit 可以自動將轉換節點新增至拓撲。 這些會顯示為 [ **拓撲] 窗格** 上的藍色方塊。

拓撲輸入和輸出在節點邊緣以黑色方塊表示。 節點的 *輸入* 會顯示在節點的左側，而 *節點的輸出* 則位於節點的右側。

拓撲節點是透過節點連線來連接，此 *連接* 會以黑色線條的形式出現，將一個節點的節點輸入連接到另一個節點的節點輸出。

下圖顯示音訊來源的連線拓撲。

![顯示從來源節點到兩個轉換節點，然後再到輸出節點之連接的圖例](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

本節包含下列主題：



| 主題                                                                                          | 描述                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [使用 TopoEdit 新增來源節點](adding-source-nodes-with-topoedit.md)                     | 描述將來源節點新增至拓撲的程式。    |
| [使用 TopoEdit 新增轉換節點](adding-transform-nodes-with-topoedit.md)               | 描述將「轉換」節點新增至拓撲的流程。 |
| [使用 TopoEdit 新增輸出節點](adding-output-nodes-with-topoedit.md)                     | 描述將輸出節點加入拓撲的程式。    |
| [連接和中斷連線拓撲節點](connecting-and-disconnecting-topology-nodes.md) | 描述連接兩個節點的進程。                 |
| [使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)                   | 描述拓撲解析的流程。                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



