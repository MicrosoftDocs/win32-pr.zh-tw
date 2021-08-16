---
description: 寫入轉換篩選
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: 寫入轉換篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816835"
---
# <a name="writing-transform-filters"></a>寫入轉換篩選

本節說明如何撰寫轉換篩選，定義為只有一個輸入 pin 和一個輸出 pin 的篩選。 為了說明這些步驟，本節描述的假設轉換篩選會輸出執行長度 (RLE) 影片的編碼。 它不會描述 RLE 編碼演算法本身，只會描述 DirectShow 特定的工作。  (DirectShow 已經透過[AVI 壓縮](avi-compressor-filter.md)程式篩選器提供了 RLE 編解碼器。 ) 

本節假設您將使用 DirectShow 基礎類別庫來建立篩選準則。 雖然您可以寫入篩選器，但強烈建議使用基底類別庫。

> [!Note]  
> 寫入轉換篩選器之前，請考慮 (DMO) 是否符合您的需求的 DirectX 媒體物件。 DMOs 可以進行許多與篩選相同的動作，而 DMOs 的程式設計模型比較簡單。 DMOs 是透過[DMO 包裝](dmo-wrapper-filter.md)函式篩選 DirectShow 裝載在，但也可以在 DirectShow 之外使用。 DMOs 現在是適用于編碼器和解碼器的建議解決方案。

 

本節包含下列主題：

-   [步驟1。選擇基類](step-1--choose-a-base-class.md)
-   [步驟2。宣告篩選類別](step-2--declare-the-filter-class.md)
-   [步驟3。支援媒體類型的協商](step-3--support-media-type-negotiation.md)
-   [步驟4：設定配置器屬性](step-4--set-allocator-properties.md)
-   [步驟5。轉換映射](step-5--transform-the-image.md)
-   [步驟6：新增對 COM 的支援](step-6--add-support-for-com.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 DirectShow 篩選](building-directshow-filters.md)
</dt> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



