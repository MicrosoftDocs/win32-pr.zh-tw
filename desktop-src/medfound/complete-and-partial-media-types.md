---
description: 本主題說明完整媒體類型與部分媒體類型之間的差異。
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: 完成和部分媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514344"
---
# <a name="complete-and-partial-media-types"></a>完成和部分媒體類型

本主題說明完整媒體類型與部分媒體類型之間的差異。

## <a name="complete-media-types"></a>完整媒體類型

完整的媒體類型是 *完整* 定義媒體資料流程格式的類型。 由於有完整的媒體類型，管線元件可以剖析與媒體類型相關聯的資料流程資料，而不會有任何混淆。

針對未壓縮的格式，下列主題會定義完整媒體類型所需的屬性：

-   音訊： [未壓縮的音訊媒體類型](uncompressed-audio-media-types.md)
-   影片： [未壓縮的影片媒體類型](uncompressed-video-media-types.md)

針對壓縮的 (或 *編碼* 的) 資料流程，完整媒體類型的定義是由編解碼器定義。 但是，如果壓縮的資料流程知道任何未壓縮的型別屬性，則這些值應該包含在壓縮資料流程的媒體類型中。 例如，如果畫面格大小是已知的，即使技術上已壓縮的資料流程沒有框架大小，也請在媒體類型上設定 [ [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md) ] 屬性。

## <a name="partial-media-types"></a>部分媒體類型

*部分* 媒體類型缺少完整媒體類型所需的一或多個屬性。 列舉可能的媒體類型時，Microsoft 媒體基礎元件可能會將值保留為未設定，表示它可以處理任何值。 例如，視頻處理器可能會將 [ [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) ] 屬性設定為 [未設定]，表示它可以處理任何畫面播放速率，並且會視需要執行畫面播放速率轉換。

如果您建立部分媒體類型，您仍然應該包含所需的資訊。 不過，媒體類型不得包含不確定的資訊。 較不正確的資訊會遺失。

部分媒體類型至少應該包含兩個屬性： [**MF \_ mt \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) 和 [**mf \_ mt \_ 子**](mf-mt-subtype-attribute.md)類型。

有時媒體基礎元件必須提供完整的媒體類型：

-   媒體來源必須提供完整的輸出類型。
-   在設定輸入類型之後，必須提供完整的輸出類型。 在設定輸入類型之前，解碼器可以提供部分輸出類型。
-   編碼器必須在設定輸出類型之後，提供完整的輸入類型。 在設定輸出類型之前，編碼器可能會提供部分輸入類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 



