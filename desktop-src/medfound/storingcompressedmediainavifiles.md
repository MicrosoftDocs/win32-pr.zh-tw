---
description: 說明如何將 Windows 媒體資料儲存在 AVI 檔案中。
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: '將壓縮的媒體儲存在 AVI 檔案中 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d52c33f6ea01cd1a10572294eaf3ee57ab4423567e3b2cc1f0feb86e199707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057723"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>將壓縮的媒體儲存在 AVI 檔案中 (Microsoft 媒體基礎) 

您使用 Windows Media 音訊和影片編解碼器壓縮的任何內容，都必須以某些容器格式放置。 其中一種最受歡迎的格式是音訊影片交錯或 AVI。 您可以使用 microsoft Video for Windows (VfW) 或 microsoft DirectShow 建立 AVI 檔案。 如需有關使用影片進行 Windows 或 DirectShow 的詳細資訊，請參閱 MSDN 上的產品檔。

已開發 Windows Media 音訊和影片編解碼器，以使用 Advanced Systems 格式的屬性 (ASF) ，也就是 Windows 媒體所使用的容器。 由於 avi 和 ASF 儲存內容的方式不同，因此將以 Windows Media 音訊和視頻編解碼器壓縮的內容儲存在 AVI 檔案中時，會發生一些問題。

Windows Media 音訊編解碼器會壓縮音訊內容，使其無法正確解壓縮，而不會有個別樣本的時間戳記。 這可讓壓縮的媒體進行一些優化。 因為 ASF 容器會將時間戳記與所有範例保持在一起，所以音訊演算法的這個特性一直都是正常運作。

不過，AVI 檔案並不會保留時間戳與範例。 這表示，當儲存在 AVI 檔案時，Windows Media 音訊內容無法正確解壓縮。 Windows媒體影片內容沒有這項限制，而且可以包含在 AVI 檔案中。 若要使用同步處理的音效將 Windows Media 視訊內容編碼為 AVI 檔案，您必須使用另一個音訊編解碼器。

使用 AVI 檔案做為 Windows 媒體容器的另一個問題，就是要考慮低位速率的影片。 Windows Media 視訊編解碼器為低位費率產生影片內容的其中一種方式，是卸載重複的畫面格。 如果您想要將 Windows Media 視訊內容放在 ASF 檔案中，您需要設定編碼器，以提供重複畫面格的虛擬框架 (將[MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md)設定為 VARIANT \_ TRUE) ，以便在檔案中表示每個畫面格。 編解碼器所產生的虛擬框架大小為8個位元組。 不過，AVI 多工器寫入檔案的框架可能會大為數百個位元組，並填滿亂數據。 以這種方式建立的 AVI 檔案仍可供播放，但會比預期更大。 您可以使用較高的位元速率來編碼儲存在 AVI 檔案中的影片，以避免這個問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 



