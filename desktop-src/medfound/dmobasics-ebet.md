---
description: DMO基礎
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: 'DMO基本 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742357"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO基本 (Microsoft 媒體基礎) 

本主題提供 DMOs 的簡短總覽，因為它們與 Windows 媒體編解碼器有關。 如需 DMOs 的詳細資訊，請參閱 [DirectX 媒體物件](../directshow/directx-media-objects.md)。

DMO 是轉換資料的 COM 物件。 您將資料傳遞給它，它會傳回已轉換的資料。 在編解碼器編碼器 DMO 的情況下，您會輸入未壓縮的媒體資料，而 DMO 會提供壓縮的媒體資料。 使用 DMOs 的主要優點是它們都是採用相同的基底介面 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)，因為您可以使用相同的物件，而不考慮正在執行的轉換類型。

因為任何類型的資料轉換都有相關的變數，所以音訊和影片轉換必須考慮各種可能的媒體配置。 Windows Media 音訊和影片編解碼器也支援一些您必須能夠使用 DMO 來設定的特殊功能。

一般而言，編解碼器 DMOs 壓縮和解壓縮數位媒體所需的變數資訊，會以下列三種方式之一進行傳達：

-   設定 DMO 的輸入類型，以傳達您傳遞給編碼器 DMO 的未壓縮媒體特性，以及您傳遞給解碼器 DMO 的壓縮媒體特性。
-   在 DMO 上設定輸出類型，以傳達編碼器 DMO 所提供的壓縮媒體特性，以及由解碼器 DMO 傳遞的未壓縮媒體特性。
-   使用 **IPropertyBag** 介面的方法，將支援編解碼器 DMOs 各項功能的其他設定設定為屬性。 **IPropertyBag** 是所有編解碼器 DMOs 都支援的標準 COM 介面。

此外，某些編解碼器功能是使用編解碼器 DMOs 特定的其他介面來管理。 在 [編解碼器物件](codecobjects.md)的區段中，會列出每個編解碼器的這些介面。

輸入和輸出類型是輸入和輸出資料流程特有的。 每個串流都代表內容的離散標記法。 例如，Windows Media 視訊編碼器 DMO 具有單一輸入資料流程，以及兩個輸出資料流程。 輸入資料流程接受未壓縮的影片範例。 這兩個輸出資料流程中的第一個會提供壓縮的範例;另一個則提供未壓縮的範例。 一個輸出資料流程中的個別樣本表示與另一個資料流程中對應樣本相同的內容，但每個資料流程會以不同的格式傳遞這些範例。

每個資料流程 (輸入或輸出) 支援一或多種類型的媒體。 媒體類型或格式是由 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構所描述。 您可以藉由呼叫 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)，查詢輸出資料流程所支援之類型的 DMO。 在某些情況下，這個方法會傳回有效的 (，但在某些情況下，該資料流程) 輸出類型部分不完整。 您可以對 **GetOutputType** 進行重複呼叫，藉此列舉輸出資料流程支援的媒體類型，並在每次呼叫時遞增類型參數。 當您傳遞的型別索引超出範圍時，方法會傳回 **DMO \_ \_ 沒有 \_ 其他 \_ 專案**。 您可以使用 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) 方法，以相同的方式列舉輸入格式。

DMO 所列舉的型別只是「慣用」類型，不過，也可能支援其他類型。 您可以藉由呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)來驗證輸出類型。 使用 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) 來驗證輸入類型。 如果您傳遞的 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構無效，這兩種方法都會傳回 **\_ \_ \_ 不 \_ 接受的 DMO E 類型**。 某些 DMOs 會要求您在列舉任何輸入類型之前，先設定輸出類型。 Windows Media 音訊和 Video 編解碼器 DMOs 都具有具有相互依存驗證的輸入和輸出。 也就是說，您設定的輸出類型將會設定輸入類型的驗證準則。 另外還有一些屬性，會在設定時改變有效的輸入和輸出類型。 基於這個理由，您應該先在 DMO 上設定所有所需屬性，再列舉類型。

當您設定 DMO 的輸出和輸入類型時，就可以開始處理範例。 每個輸入範例都會使用 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)的呼叫傳遞給編解碼器，而當您呼叫 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)時，每個輸出範例都會由編解碼器傳遞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
