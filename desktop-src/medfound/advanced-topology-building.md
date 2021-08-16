---
description: Advanced 拓朴建築
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Advanced 拓朴建築
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664868"
---
# <a name="advanced-topology-building"></a>Advanced 拓朴建築

本節說明一些建立拓撲的先進技術。 如果您想要更充分掌控傳送至媒體會話的拓撲，您可以使用這些技術。

因為這些技術適用于超越標準拓撲載入器所提供之功能的案例，所以許多詳細資料將取決於您應用程式的特定需求。 因此，本節會在較小的子工作（而不是完整的端對端案例）上以鬆散的方式組織。

一般的播放應用程式會遵循下列步驟：

1.  應用程式會建立部分拓撲，並在媒體會話上將它排入佇列。
2.  媒體會話會叫用拓撲載入器來解析拓撲。

如果您想要超越拓撲載入器的功能，有三種常見的方法：

-   建立完整的拓撲。 當您將拓撲排入媒體會話的佇列時，請使用 MFSESSION SetTopology NORESOLUTION 旗標呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) \_ \_ 。 此旗標可防止媒體會話嘗試解析拓撲。

-   直接叫用拓撲載入器來解析拓撲。 然後，您可以修改完整拓撲，然後將它排入媒體會話的佇列。

-   執行自訂拓撲載入器。 使用這個方法，您可以將部分拓撲排在佇列中，但是媒體會話會叫用您的自訂載入器，而不是標準媒體基礎的執行。 這種方法的其中一個優點是您可以在受保護的環境內執行自訂拓撲建立。 不過，在這種情況下 (，拓撲載入器必須是受信任的元件。 如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。 ) 

此章節包含下列主題。



| 主題                                                                          | 描述                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [自訂拓撲載入器](custom-topology-loaders.md)                         | 如何針對媒體會話提供 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 的自訂執行。          |
| [將輸出節點系結至媒體接收](binding-output-nodes-to-media-sinks.md) | 如果您在媒體會話之外使用拓撲載入器，如何準備拓撲中的輸出節點。 |
| [將解碼器新增至拓撲](adding-a-decoder-to-a-topology.md)           | 如何手動選取解碼器，然後將它新增至拓撲。                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[拓撲](topologies.md)
</dt> </dl>

 

 



