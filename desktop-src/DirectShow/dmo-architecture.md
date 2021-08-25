---
description: DMO建築
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO建築
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2e125fda635c70e03e02af15d12e0ffb4f3ac4d5083eb91a4b99d3d3590e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906488"
---
# <a name="dmo-architecture"></a>DMO建築

本節說明 DMO 的整體架構。

**串流**

DMO 是接受 *m* 輸入並產生 *n* 輸出的物件。 輸入和輸出稱為 *資料流程*。 每個 DMO 都至少有一個資料流程。 資料流程不是物件;它們只會依索引編號在 DMO 上參考。 資料流程的數目會在設計階段修正。

**媒體類型**

所有資料都是使用 *媒體類型* 來輸入，它會定義如何解讀資料的內容。 例如，320 x 240 24 位 RGB video 是一種類型;44.1-千赫茲 (kHz) 16 位身歷聲 PCM 音訊是另一種類型。 媒體類型是使用 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構來描述。 在用戶端可以處理任何資料之前，它必須在 DMO 上設定每個資料流程的媒體類型。

一般而言，資料流程可以接受一系列的媒體類型。 有些 DMOs 支援比其他類型更廣泛的型別。 DMO 介面會定義方法，讓用戶端探索支援的類型。 例如，一個 DMO 可支援任何位深度的 RGB 影片，而另一個則可能只支援24位 rgb。 此外，DMO 可能僅限於特定的輸入和輸出組合。 例如，如果輸入類型是16位的影片，則輸出資料流程可能需要相同的位深度。 用戶端可以列舉每個資料流程的慣用類型，然後測試特定的組合。

**緩衝區**

在預設的 DMO 模型中，用戶端會配置個別的輸入緩衝區和輸出緩衝區。 它會以資料填滿輸入緩衝區，並將其傳遞至 DMO，而 DMO 會將新的資料寫入至輸出緩衝區。

（選擇性） DMO 可以支援「就地」處理。 透過就地處理，DMO 會將輸出直接寫入至輸入緩衝區，而不是原始資料。 就地處理無須個別的緩衝區。 相反地，它會改變原始資料，有些應用程式可能無法接受。

預設 (非就地) 緩衝模型是透過 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面支援。 所有 DMOs 都必須執行這個介面。 如果 DMO 支援就地處理，它也會公開 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace)介面。 用戶端負責配置所有緩衝區，包括輸入和輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DMOs](about-dmos.md)
</dt> </dl>

 

 



