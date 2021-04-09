---
description: 描述您可以從 Windows Media 編解碼器取出的統計資料。
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: '取得編碼統計資料 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689287"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>取得編碼統計資料 (Microsoft 媒體基礎) 

編碼會話中發生之情況的相關資訊，通常會立即以處理範例時傳回的錯誤碼形式提供。 不過，您可以從編解碼器取得有關各種編碼方面的統計資料。

## <a name="video-frame-information"></a>影片畫面資訊

您可以取出的部分影片統計資料會處理編碼器所處理的畫面格數。 您可以從影片編碼器讀取三個框架編號屬性：

-   [MFPKEY \_TOTALFRAMES](mfpkey-totalframesproperty.md) 是透過輸入資料流程處理的框架數。
-   [MFPKEY \_CODEDFRAMES](mfpkey-codedframesproperty.md) 是已編碼的框架數目。 藉由從傳遞的框架總數減去此值，您可以判斷已卸載的框架數。
-   [MFPKEY \_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) 是未編碼的框架數目，因為它們已包含重複的內容。 此值不會從 < i 部所報告的編碼框架數目減去。

在編碼期間，您可以隨時讀取影片畫面的屬性。 這有助於判斷編碼設定是否適用于您的內容;如果總畫面格和程式碼框架之間有很大的差異，則壓縮的內容可能不符合您的品質需求。 完成編碼之後，您可以讀取最終的值。

## <a name="vbr-buffer-statistics"></a>VBR 緩衝區統計資料

根據所使用的編碼模式而定，部分或全部的緩衝區設定可能會在編碼期間決定 (例如，在將內容編碼) 之前，不知道以品質為基礎之 VBR 的位元速率。 您可以使用 **IPropertyBag：： Read** 方法取得四個 VBR 緩衝區屬性：

-   [MFPKEY \_RAVG](mfpkey-ravgproperty.md) 是 VBR 內容的平均位元速率。
-   [MFPKEY \_BAVG](mfpkey-bavgproperty.md) 是平均位元速率的緩衝區視窗。
-   [MFPKEY \_RMAX](mfpkey-rmaxproperty.md) 是 VBR 內容的尖峰位元速率。
-   [MFPKEY \_BMAX](mfpkey-bmaxproperty.md) 是尖峰緩衝區視窗。

開始處理範例之後，除非您已完成串流的編碼，否則不應讀取任何 VBR 屬性。 如果您這樣做，編碼器會將您的要求視為編碼完成的信號來解讀。 您處理的下一個範例會被視為新的編碼會話。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 



