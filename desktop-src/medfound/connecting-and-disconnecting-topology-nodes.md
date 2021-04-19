---
description: 連接和中斷連線拓撲節點
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: 連接和中斷連線拓撲節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991663"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>連接和中斷連線拓撲節點

若要讓拓撲正常運作，必須連接來源節點和輸出節點。 若要連接兩個拓撲節點，請將一個節點的節點輸出拖曳至另一個節點的節點輸入。 TopoEdit 會以黑線顯示節點連接。 這相當於藉由呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) 方法來連接拓撲節點。

只有當節點連接有效時，才可以解析拓撲;亦即，如果兩個節點的媒體類型相容。 如需有關解決拓撲的詳細資訊，請參閱 [使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)。

如果您嘗試從已經連接的節點建立連線，新的節點連接會取代舊的節點連接。

若要刪除連線，請選取節點連接，然後按下 DELETE 鍵，或從 [**拓撲**] 功能表中選取 [**刪除**]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 TopoEdit 建立拓撲](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



