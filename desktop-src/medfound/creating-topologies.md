---
description: 建立拓撲
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: 建立拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4048200055066a601f9044ff109f173cb00fc4449a71ea1331b29c8be1a59b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777618"
---
# <a name="creating-topologies"></a>建立拓撲

本節說明一些建立拓撲的一般程式。

建立拓撲的一般步驟如下：

1.  藉由呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)來建立新的拓撲物件。 此函式會傳回拓撲的 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面指標。

2.  一開始，拓撲不包含任何節點。 若要建立拓撲的節點，請呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode)。 此函式會傳回節點 [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) 介面的指標。 您必須在建立節點時指定節點類型：

    -   來源節點。

    -   轉換節點。

    -   輸出節點。

    -   T 節點。

3.  初始化每個節點。 初始化程式依節點類型而定，如下列主題所述。

4.  藉由呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode)，將每個節點新增至拓撲。

5.  連線節點。 若要連接節點，請在上游節點上呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) ，並傳入下游節點的指標。

下列主題提供每個節點類型的特定步驟。



| 主題                                                    | 描述                     |
|----------------------------------------------------------|---------------------------------|
| [建立來源節點](creating-source-nodes.md)       | 如何建立來源節點。    |
| [建立轉換節點](creating-transform-nodes.md) | 如何建立轉換節點。 |
| [建立輸出節點](creating-output-nodes.md)       | 如何建立輸出節點。   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[拓撲](topologies.md)
</dt> </dl>

 

 



