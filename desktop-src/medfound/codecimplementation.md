---
description: 編解碼器實行。
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Codec 實作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974857"
---
# <a name="codec-implementation"></a>Codec 實作

Windows Media 音訊和影片編解碼器會實作為 COM 物件。 一般而言，編解碼器會實作為一對 COM 物件：一個用於編碼器，另一個用於解碼器。 編碼器)  (CLSID 的類別識別碼，而該編碼器具有不同的 CLSID。 例如，Windows Media 音訊9編解碼器的編碼器部分具有以常數 **clsid \_ CWMAEncMediaObject** 表示的 clsid，而該相同編解碼器的編碼器部分具有以常數 **clsid \_ CWMADecMediaObject** 表示的 clsid。

在某些情況下，單一 COM 物件中包含一個以上的編碼器。 例如，Windows Media 視訊9編碼器和 Windows Media 視訊9.1 編碼器都是相同 COM 物件的一部分。 因此，它們都有相同的 CLSID，以常數 **CLSID \_ CWMV9EncMediaObject** 表示。 同樣地，某些 COM 物件包含一個以上的解碼器。

每個編碼器或解碼物件都會公開 [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29)介面，讓物件可以作為 DirectX 媒體物件使用 (DMO) 和 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面，讓物件可以作為媒體基礎轉換 (MFT) 使用。

對於大部分的編碼器而言，不論您是使用編碼器做為 DMO 或 MFT，您都可以使用相同的 CLSID 來建立編碼器的實例。 例如，若要建立 Windows Media 視訊9編碼器的實例，您可以使用 **CLSID \_ CWMV9EncMediaObject**，不論您是否想要使用編碼器作為 DMO 或 MFT。 同樣地，對於大部分的解碼器而言，不論您使用的是 DMO 還是 MFT，每個解碼器都會有單一 CLSID。

> [!Note]  
> 上述語句有一些例外狀況，有關使用 DMO 和 MFT 的單一 CLSID。 例如，當 mpeg-2 第2部分的 clsid 做為 DMO 時，會有一個 clsid，而當其作為 MFT 時，則會有不同的 clsid。

 

除了核心介面外，每個編碼器或編解碼器物件都會執行兩個類似的介面，以使用編解碼器屬性（ **IPropertyBag** 和 **IPropertyStore**）。 較舊版本的編碼器和解碼器物件使用 **IPropertyBag**，它會依包含屬性名稱的字串值來識別每個屬性。 **IPropertyStore** 是較新的介面，用來識別具有唯一屬性索引鍵值的屬性。 已新增 **IPropertyStore** 的支援，以提供對 MFTs 的支援。 大部分 **IPropertyBag** 的屬性名稱字串都有對應的 **IPropertyStore** 屬性索引鍵 GUID，而大部分的 guid 都有對應的 **IPropertyBag** 名稱字串，但有一些例外狀況。

本檔會依屬性索引鍵常數列出屬性，但每個專案都包含屬性名稱字串常數，以便在適當時與 **IPropertyBag** 搭配使用。

## <a name="related-topics"></a>相關主題

[Windows Media 轉碼器](windows-media-codecs.md)
