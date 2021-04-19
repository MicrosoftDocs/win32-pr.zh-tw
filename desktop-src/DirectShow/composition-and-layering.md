---
description: 撰寫和分層
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: 撰寫和分層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967005"
---
# <a name="composition-and-layering"></a>撰寫和分層

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

在一組追蹤的集合中，第一個軌的優先順序最低 (優先順序 0) ，而且每個後續的播放軌都有一個較高的優先權層級。 在每個優先權層級，該追蹤中的來源剪輯會隱藏其下追蹤中的來源剪輯，除非該圖層也包含轉換。 因此，您可以想像 DES 在轉譯時進行數次傳遞。

首先，它會呈現 track 0。 在「追蹤0」底下沒有任何專案，因此空白區域會轉譯為實心黑色影像。 此圖層中的轉換會在黑色影像和軌0之間進行，反之亦然。 DES 會在曲目0的上方配置追蹤1，在兩個曲目之間產生任何轉換。 結果就是兩個追蹤的複合。 接下來，它會將追蹤2放到這個複合。 這一層的轉換會在複合和 track 2 之間進行。 此程式會繼續進行，直到最後一個 (最高優先順序的) 追蹤為止。

當有多個追蹤組合在一起時，它們的行為就像是單一追蹤 (稱為「虛擬追蹤) 」。 組合物件會封裝此行為，因此可以進行複雜的轉換。 例如，一個影片剪輯可以抹除至第二個剪輯，而複合 (兩個剪輯加上抹除) 淡化為第三個剪輯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務開始使用](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



