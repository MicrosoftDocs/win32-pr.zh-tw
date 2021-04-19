---
description: In-Place 處理
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place 處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970296"
---
# <a name="in-place-processing"></a>In-Place 處理

您可以直接修改資料來完成特定的資料轉換。 這稱為就地 *處理。* 許多音訊和影片效果都可以透過這種方式來完成。 如果 SQL-DMO 支援就地處理，它會公開 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) 介面。 就地處理比針對輸出使用不同的緩衝區，通常更有效率。  (一個主要的例外狀況是當緩衝區位於視訊記憶體時。 在這種情況下，讀取作業的速度會比寫入作業慢很多，因此不建議就地處理。 ) 

若要就地處理資料，用戶端會對 [**IMediaObjectInPlace：:P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) 方法進行單一呼叫，而不是個別呼叫 **ProcessInput** 和 **ProcessOutput**。 **Process** 方法是同步的;所有處理都是在呼叫內進行。 此外，就地處理不會使用 **IMediaBuffer** 物件。 **Process** 方法會將指標直接帶到記憶體緩衝區。

支援就地處理的 SQL-DMO 仍必須執行 **IMediaObject** 介面，包括 **ProcessInput** 和 **ProcessOutput** 方法。 用戶端可以選擇是要使用就地處理或使用不同的緩衝區。 不過，請勿混用這兩種類型的處理。 如果您呼叫 **進程**，請勿呼叫 **ProcessInput** 或 **ProcessOutput**，反之亦然。

**效果連接結尾**

在輸入停止後，可能會建立一些額外的輸出。 這稱為 *效果結尾*。 例如，當輸入進入無回應後，就會繼續執行回音效果。 如果有效果結尾，則 **Process** 方法會傳回 \_ FALSE。 當應用程式處理其所有資料之後，它就可以將空的緩衝區傳送至 **Process** 方法，以產生效果結尾。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[直接裝載](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



