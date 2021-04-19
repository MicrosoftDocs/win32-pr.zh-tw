---
description: 關於媒體範例和配置器
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: 關於媒體範例和配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991946"
---
# <a name="about-media-samples-and-allocators"></a>關於媒體範例和配置器

篩選會跨 pin 連接傳遞資料。 資料會從一個篩選的輸出圖釘移至另一個篩選的輸入圖釘。 輸出圖釘傳遞資料的最常見方式，是在輸入上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法，雖然另外還有一些其他機制也存在。

根據篩選準則，媒體資料的記憶體可以不同的方式配置：在堆積上、DirectDraw 介面、使用共用的 GDI 記憶體，或使用其他的配置機制。 負責配置記憶體的物件稱為配置 *器，它* 是公開 [**IMEMALLOCATOR**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的 COM 物件。

當兩個 pin 連接時，其中一個 pin 必須提供配置器。 DirectShow 定義了一系列的方法呼叫，用來建立配置器所提供的 pin。 釘選也會同意配置器將建立的緩衝區數目，以及緩衝區的大小。

開始串流之前，配置器會建立緩衝區集區。 在串流處理期間，上游篩選器會將資料填入緩衝區，並將其傳遞至下游篩選器。 但上游篩選不會將下游篩選器的原始指標提供給緩衝區。 相反地，它會使用稱為「 *媒體範例*」的 COM 物件，而配置器會建立這些物件來管理緩衝區。 媒體範例會公開 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面。 媒體範例包含：

-   基礎緩衝區的指標
-   時間戳記
-   各種旗標
-   （選擇性）媒體類型

時間戳記會定義轉譯器篩選器用來排程轉譯的呈現時間。 旗標指出自上一個範例之後，資料中是否有中斷的情況。 媒體類型提供一種方式，讓篩選器變更中間資料流程的格式。 通常，此範例不會有媒體類型，這表示格式自上一個範例之後未變更。

當篩選使用緩衝區時，它會保存範例上的參考計數。 配置器會使用參考計數來決定何時可以重複使用緩衝區。 這可防止篩選覆寫另一個篩選仍在使用中的緩衝區。 在每個篩選器發行之前，範例都不會回到配置器的可用樣本集區。

如需詳細資訊，請參閱下列主題：

-   主題 [範例和配置器](samples-and-allocators.md) 提供配置器運作方式的詳細描述。
-   [篩選圖形中](data-flow-in-the-filter-graph.md)的主題資料流程提供有關 DirectShow 中資料流程的一般總覽。

下列主題適用于撰寫自己的自訂篩選器的開發人員：

-   [篩選開發人員的資料流程](data-flow-for-filter-developers.md)
-   [執行緒和重要區段](threads-and-critical-sections.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選圖形及其元件](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



