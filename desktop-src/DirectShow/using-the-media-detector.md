---
description: 使用媒體偵測器
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: 使用媒體偵測器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974755"
---
# <a name="using-the-media-detector"></a>使用媒體偵測器

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

媒體偵測器是一種協助程式物件，可取得檔案的相關資訊，例如資料流程的數目、類型和持續時間。 它也包含從影片串流中取出海報框架的方法。 它會公開 [**IMediaDet**](imediadet.md) 介面。

媒體偵測器會以兩種模式的其中一種方式運作。 當您建立媒體偵測器的實例時，它不會附加至特定的原始程式檔。 在此模式中，您可以從多個來源檔案取出串流資訊。 不過，一旦您使用媒體偵測器來取得海報框架，它就會切換為 *點陣圖抓取模式*。 在點陣圖抓取模式中，媒體偵測器會附加至特定的影片資料流程，而資料流程資訊方法將無法再運作。 此外，也沒有辦法將媒體偵測器切換回其啟動模式。 因此，在您取得海報框架之前，請先取得所需的任何串流資訊，或者為每個串流建立新的媒體偵測器實例。

若要取得串流資訊，請執行下列動作：

1.  以原始程式檔的名稱呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md) ]。
2.  呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) 取得來源中的資料流程數目。
3.  使用 IMediaDet 指定串流號碼 [**：:p 的 \_ CurrentStream**](imediadet-put-currentstream.md)。 然後呼叫下列一或多個方法：
    -   [**IMediaDet：： get \_StreamType**](imediadet-get-streamtype.md)：抓取資料流程的媒體類型。
    -   [**IMediaDet：： get \_StreamLength**](imediadet-get-streamlength.md)：抓取資料流程的持續時間。
    -   [**IMediaDet：： get \_幀**](imediadet-get-framerate.md)速率：抓取視頻資料流程的畫面播放速率。

若要取得海報框架，請指定串流號碼，如同上一個步驟所示。 然後呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md)，將海報框架複製到緩衝區，或呼叫 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)，以將海報框架儲存至檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用來源](working-with-sources.md)
</dt> </dl>

 

 



