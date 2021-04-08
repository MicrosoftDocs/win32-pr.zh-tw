---
title: 音樂檔案的屬性
description: 音樂檔案的屬性
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性、音訊檔
- 屬性、音樂檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672044"
---
# <a name="attributes-for-music-files"></a>音樂檔案的屬性

本節列出常用於包含音樂之音訊檔案的屬性。 建議您根據這些清單設定檔案的屬性，以確保您的檔案與各種不同的播放應用程式完全相容。 此區段中的屬性會以三種類別列出：主要、次要和第三個類別。

主要屬性會傳達最基本的檔案相關資訊。 如果您要建立用於散發的音訊檔案，這是您應該使用的最小屬性集。

次要屬性包含對所有音訊檔案而言很重要，但不是通用的通用中繼資料。

第三個屬性應該包含在必要的情況下，但不是描述檔案的必要條件。

## <a name="primary-attributes-for-music"></a>音樂的主要屬性

-   [**作者**](author.md)
-   [**標題**](title.md)
-   [**WM/AlbumArtist**](wm-albumartist.md)
-   [**WM/ContentDistributor**](wm-contentdistributor.md)
-   [**WM/內容類型**](wm-genre.md)
-   如果有 (，則為 [**WM/MCDI**](wm-mcdi.md)否則，請使用 [**wm/WMCollectionID**](wm-wmcollectionid.md)、 [**wm/WMCollectionGroupID**](wm-wmcollectiongroupid.md)或 [**wm/WMContentID**](wm-wmcontentid.md)) 
-   [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
-   [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
-   [**WM/提供者**](wm-provider.md)
-   [**WM/TrackNumber**](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a>音樂的次要屬性

-   [**著作權**](copyright.md)
-   [**WM/編輯器**](wm-composer.md)
-   [**WM/EncodingTime**](wm-encodingtime.md)
-   [**WM/語言**](wm-language.md)
-   [**WM/ParentalRating**](wm-parentalrating.md)
-   [**WM/生產者**](wm-producer.md)
-   [**WM/工具**](wm-toolname.md)
-   [**WM/ToolVersion**](wm-toolversion.md)
-   [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)
-   [**WM/WMCollectionID**](wm-wmcollectionid.md)
-   [**WM/WMContentID**](wm-wmcontentid.md)
-   [**WM/Writer**](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a>音樂的第三個屬性

-   [**描述**](description.md)
-   [**WM/AuthorURL**](wm-authorurl.md)
-   [**WM/BeatsPerMinute**](wm-beatsperminute.md)
-   [**WM/導體**](wm-conductor.md)
-   [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)
-   [**WM/EncodedBy**](wm-encodedby.md)
-   [**WM/EncodingSettings**](wm-encodingsettings.md)
-   [**WM/InitialKey**](wm-initialkey.md)
-   [**WM/歌詞**](wm-lyrics.md)
-   [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md)
-   [**WM/情緒**](wm-mood.md)
-   [**WM/PartOfSet**](wm-partofset.md)
-   [**WM/句號**](wm-period.md)
-   [**WM/圖片**](wmpicture.md)
-   [**WM/PromotionURL**](wm-promotionurl.md)
-   [**WM/發行者**](wm-publisher.md)
-   [**WM/子標題**](wm-subtitle.md)
-   [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)
-   [**WM/UserWebURL**](wm-userweburl.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**依類型的屬性**](attributes-by-type.md)
</dt> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




