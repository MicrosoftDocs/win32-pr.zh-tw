---
description: 瞭解 Microsoft 媒體基礎中的媒體類型。 媒體類型描述媒體資料流程的格式。
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: '關於媒體類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263c2b473e378e6ae5dc75453b20d02dce61818f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010901"
---
# <a name="about-media-types-microsoft-media-foundation"></a>關於媒體類型 (Microsoft 媒體基礎) 

*媒體類型* 描述媒體資料流程的格式。 在 Microsoft 媒體基礎中，媒體類型會以 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面表示。 這個介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 媒體類型的詳細資料會指定為屬性。

若要建立新的媒體類型，請呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 函數。 此函數會傳回 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。 媒體類型一開始沒有任何屬性。 若要設定格式的詳細資料，請設定相關的屬性。

如需媒體類型屬性的清單，請參閱 [媒體類型屬性](media-type-attributes.md)。

## <a name="major-types-and-subtypes"></a>主要類型和子類型

任何媒體類型的兩項重要資訊是主要類型和子類型。

-   *主要類型* 是 GUID，可定義媒體資料流程中資料的整體分類。 主要類型包括影片和音訊。 若要指定主要類型，請設定 [ [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) ] 屬性。 [**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)方法會傳回這個屬性的值。
-   *子類型* 會進一步定義格式。 例如，在影片主要類型中，有 RGB-24、RGB-32、YUY2 等等的子類型。 在音訊中，有 PCM 音訊、IEEE 浮點音訊及其他。 子類型提供的資訊高於主要類型，但不會定義格式的所有內容。 例如，影片子類型不會定義影像大小或畫面播放速率。 若要指定子類型，請設定 [ [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md) ] 屬性。

所有媒體類型都應該有主要類型 GUID 和子類型 GUID。 如需主要類型和子類型 Guid 的清單，請參閱 [媒體類型 guid](media-type-guids.md)。

## <a name="why-attributes"></a>為什麼要有屬性？

相較于先前的技術（例如 DirectShow 和 Windows Media Format SDK）所使用的格式結構，屬性有幾個優點。

-   更容易表示「不知道」或「不在意」的值。 例如，如果您要撰寫影片轉換，您可能事先知道轉換支援哪些 RGB 和 YUV 格式，而不是影片框架的尺寸，直到您從影片來源取得它們為止。 同樣地，您可能不在意特定的詳細資料，例如影片主要複本。 使用格式結構時，每個成員都必須填入 *某個* 值。 如此一來，使用零表示未知或預設值會很常見。 如果另一個元件將零視為合法值，這種做法可能會造成錯誤。 使用屬性時，您只需要省略未知或與您的元件無關的屬性。

-   當需求隨著時間變更時，會在結構結尾新增其他資料來擴充格式結構。 例如， **WAVEFORMATEXTENSIBLE** 會擴充 **WAVEFORMATEX** 結構。 這種作法很容易發生錯誤，因為元件必須將結構指標轉換成其他結構類型。 您可以安全地延伸屬性。
-   已定義了互相不相容的格式結構。 例如，DirectShow 定義了 **VIDEOINFOHEADER** 和 **VIDEOINFOHEADER2** 結構。 彼此獨立設定屬性，因此不會發生此問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 



