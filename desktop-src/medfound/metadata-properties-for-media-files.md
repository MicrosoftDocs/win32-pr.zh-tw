---
description: 本主題列出媒體檔案最常見的中繼資料屬性。
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: 媒體檔案的中繼資料屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981732"
---
# <a name="metadata-properties-for-media-files"></a>媒體檔案的中繼資料屬性

本主題列出媒體檔案最常見的中繼資料屬性。

-   [一般媒體屬性](#common-media-properties)
-   [媒體共用屬性](#media-sharing-properties)
-   [Windows Media Format SDK 對應](#windows-media-format-sdk-mappings)
-   [相關主題](#related-topics)

## <a name="common-media-properties"></a>一般媒體屬性

Shell 屬性系統會針對所有類型的 Shell 物件定義一組通用的中繼資料屬性。 這些檔案的子集適用于媒體檔案。 下表列出媒體最常見的 Shell 屬性。 媒體檔案可能會支援此處未列出的其他屬性。 此外，並非每個檔案格式都支援列出的每個屬性。 如需 Shell 屬性的完整清單，請參閱 [Shell 屬性](/previous-versions//ff521730(v=vs.85))。



| PROPERTYKEY                                                              | Shell 名稱                                                                                    | Description                                                                                                                                                                                               | 資料類型    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [MFPKEY \_ Content \_ DLNA \_ 設定檔 \_ 識別碼](mfpkey-content-dlna-profile-id.md) | 無                                                                                          | 數位生活網路聯盟 (DLNA) 設定檔識別碼。                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ 音訊 \_ ChannelCount**                                            | [ChannelCount](../properties/props-system-audio-channelcount.md)                       | 音訊聲道數目。                                                                                                                                                                                 | VT \_ UI4      |
| **PKEY \_ 音訊 \_ EncodingBitrate**                                         | [EncodingBitrate](../properties/props-system-audio-encodingbitrate.md)                 | 平均音訊位速率（以每秒位數為單位）。                                                                                                                                                               | VT \_ UI4      |
| **PKEY \_ 音訊 \_ 格式**                                                  | [System.string. Format](../properties/props-system-audio-format.md)                                   |  ([**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 的音訊子類型) 以字串表示。                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 音訊 \_ IsVariableBitRate**                                       | [IsVariableBitRate](../properties/props-system-audio-isvariablebitrate.md)             | 指出音訊資料流程是否使用可變的位速率編碼。                                                                                                                                       | VT \_ BOOL     |
| **PKEY \_ 音訊 \_ PeakValue**                                               | [PeakValue](../properties/props-system-audio-peakvalue.md)                             | 音訊內容的尖峰音量層級。                                                                                                                                                                       | VT \_ UI4      |
| **PKEY \_ 音訊 \_ SampleRate**                                              | [SampleRate](../properties/props-system-audio-samplerate.md)                           | 每秒樣本數的音訊取樣率。 相當於媒體類型中的 [**MF \_ MT \_ 音訊 \_ 範例（ \_ 每 \_ 秒**](mf-mt-audio-samples-per-second-attribute.md) ）屬性。                           | VT \_ UI4      |
| **PKEY \_ 音訊 \_ SampleSize**                                              | [SampleSize](../properties/props-system-audio-samplesize.md)                           | 每個音訊樣本的位數數目。 相當於媒體類型中 [**\_ \_ \_ \_ 每個 \_ 樣本屬性的 MF MT 音訊位**](mf-mt-audio-bits-per-sample-attribute.md) 。                                         | VT \_ UI4      |
| **PKEY \_ 音訊 \_ StreamNumber**                                            | [StreamNumber](../properties/props-system-audio-streamnumber.md)                       | 音訊串流的識別碼。                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ 作者**                                                         | [System.Author](../properties/props-system-author.md)                                               | 作者。                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ 批註**                                                        | [System. Comment](../properties/props-system-comment.md)                                             | 附加至檔案的批註，通常是由使用者新增。                                                                                                                                                  | VT \_ LPWSTR   |
| **PKEY \_ 著作權**                                                      | [系統著作權](../properties/props-system-copyright.md)                                         | 著作權資訊。                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ DRM \_ IsProtected**                                               | [IsProtected](../properties/props-system-drm-isprotected.md)                             | 指出內容是否使用數位版權管理 (DRM) 來保護。                                                                                                                         | VT \_ BOOL     |
| **PKEY \_ 關鍵字**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | 關鍵 字。                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 語言**                                                       | [System. Language](../properties/props-system-language.md)                                           | 語言。                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ AuthorUrl**                                               | [AuthorUrl](../properties/props-system-media-authorurl.md)                             | 作者網站的 URL。                                                                                                                                                                              | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ AverageLevel**                                            | [AverageLevel](../properties/props-system-media-averagelevel.md)                       | 音訊內容的平均音量層級。                                                                                                                                                                    | VT \_ UI4      |
| **PKEY \_ 媒體 \_ ClassPrimaryID**                                          | [ClassPrimaryID](../properties/props-system-media-classprimaryid.md)                   | GUID 的字串表示，識別媒體的主要類別。 如需有效的值，請參閱 [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md) 屬性的說明文件。       | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ ClassSecondaryID**                                        | [ClassSecondaryID](../properties/props-system-media-classsecondaryid.md)               | GUID 的字串表示，識別媒體的次要類別。 如需有效的值，請參閱 [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md) 屬性的說明文件。 | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ CollectionGroupID**                                       | [CollectionGroupID](../properties/props-system-media-collectiongroupid.md)             | 識別集合群組之 GUID 的字串表示。                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ CollectionID**                                            | [CollectionID](../properties/props-system-media-collectionid.md)                       | 識別集合之 GUID 的字串表示。                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ ContentDistributor**                                      | [ContentDistributor](../properties/props-system-media-contentdistributor.md)           | 內容的散發者。                                                                                                                                                                               | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ ContentID**                                               | [ContentID](../properties/props-system-media-contentid.md)                             | 識別集合之 GUID 的字串表示。                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ DateEncoded**                                             | [DateEncoded](../properties/props-system-media-dateencoded.md)                         | 編碼內容的時間。                                                                                                                                                                        | VT \_ FILETIME |
| **PKEY \_ 媒體 \_ DateReleased**                                            | [DateReleased](../properties/props-system-media-datereleased.md)                       | 原始發行日期。                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ 持續時間**                                                | [System.object。持續時間](../properties/props-system-media-duration.md)                               | 持續時間，以 100-毫微秒單位表示。 相當於表示描述項中的 [**MF \_ PD \_ DURATION**](mf-pd-duration-attribute.md) 屬性。                                                       | VT \_ UI8      |
| **PKEY \_ 媒體 \_ DVDID**                                                   | [DVDID](../properties/props-system-media-dvdid.md)                                     | 數位視訊光碟識別碼 (DVDID) 。                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ EncodedBy**                                               | [EncodedBy](../properties/props-system-media-encodedby.md)                             | 編碼內容的人員或組名。                                                                                                                                                     | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ EncodingSettings**                                        | [EncodingSettings](../properties/props-system-media-encodingsettings.md)               | 用來將內容編碼的設定描述。                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ MCDI**                                                    | [MCDI](../properties/props-system-media-mcdi.md)                                       | 音樂 CD 識別碼。 此值可用來識別 CD。                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ MetadataContentProvider**                                 | [MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | 中繼資料內容提供者的名稱。  (例如，中繼資料可能由商務服務提供。 )                                                                                                  | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ 生產者**                                                | [系統. 媒體生產者](../properties/props-system-media-producer.md)                               | 內容生產者的名稱。                                                                                                                                                                      | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ PromotionUrl**                                            | [PromotionUrl](../properties/props-system-media-promotionurl.md)                       | 網站的 URL，其提供與內容相關的促銷。                                                                                                                                             | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ ProviderRating**                                          | [ProviderRating](../properties/props-system-media-providerrating.md)                   | 中繼資料內容提供者所指派的內容分級。                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ ProviderStyle**                                           | [ProviderStyle](../properties/props-system-media-providerstyle.md)                     | 中繼資料內容提供者所指派內容的樣式或內容類型。                                                                                                                               | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ 發行者**                                               | [系統。發行者](../properties/props-system-media-publisher.md)                             | 簽發者。                                                                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ 副標題**                                                | [[系統] 副標題](../properties/props-system-media-subtitle.md)                               | 字幕。                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ UniqueFileIdentifier**                                    | [UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | 可以用來識別檔案的一般字串。                                                                                                                                                        | VT \_ LPWSTR   |
| **PKEY \_ 媒體 \_ 寫入器**                                                  | [系統. 媒體寫入器](../properties/props-system-media-writer.md)                                   | 作家。                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Media \_ Year**                                                    | [Year](../properties/props-system-media-year.md)                                       | 發佈內容的年份。                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ 音樂 \_ AlbumArtist**                                             | [AlbumArtist](../properties/props-system-music-albumartist.md)                         | 專輯的主要演出者。 您可以使用這個屬性來區別專輯的主要演出者與與特定曲目共同合作的演出者。                                            | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ AlbumTitle**                                              | [AlbumTitle](../properties/props-system-music-albumtitle.md)                           | 專輯標題。                                                                                                                                                                                              | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ 演出者**                                                  | [系統音樂](../properties/props-system-music-artist.md)                                   | 演出者。                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ BeatsPerMinute**                                          | [BeatsPerMinute](../properties/props-system-music-beatsperminute.md)                   | 每分鐘的節拍數。                                                                                                                                                                                         | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ 編輯器**                                                | [系統音樂編輯器](../properties/props-system-music-composer.md)                               | 作曲家。                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ 導體**                                               | [System.servicemodel](../properties/props-system-music-conductor.md)                             | 導體。                                                                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ ContentGroupDescription**                                 | [ContentGroupDescription](../properties/props-system-music-contentgroupdescription.md) | 內容群組的描述 (例如，[盒裝組] 或 [數列]) 。                                                                                                                                      | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ 類型**                                                   | [System.object](../properties/props-system-music-genre.md)                                     | 體裁。                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ InitialKey**                                              | [System.Music.InitialKey](../properties/props-system-music-initialkey.md)                           | 音樂的初始索引鍵。                                                                                                                                                                             | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ IsCompilation**                                           | [IsCompilation](../properties/props-system-music-iscompilation.md)                     | 指出音樂檔案是否為編譯的一部分。                                                                                                                                                | VT \_ BOOL     |
| **PKEY \_ 音樂 \_ 歌詞**                                                  | [歌詞](../properties/props-system-music-lyrics.md)                                   | 歌詞。                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ 音樂的 \_ 情緒**                                                    | [System.object](../properties/props-system-music-mood.md)                                       | 心情。                                                                                                                                                                                                     | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ PartOfSet**                                               | [PartOfSet](../properties/props-system-music-partofset.md)                             | 元件編號和檔案所屬集合中的部分數目，以斜線分隔。                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ 期間**                                                  | [系統音樂。](../properties/props-system-music-period.md)                                   | 時期。                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ 音樂 \_ TrackNumber**                                             | [TrackNumber](../properties/props-system-music-tracknumber.md)                         | 曲目編號。                                                                                                                                                                                             | VT \_ UI4      |
| **PKEY \_ ParentalRating**                                                 | [System. ParentalRating](../properties/props-system-parentalrating.md)                               | 家長評等。                                                                                                                                                                                          | VT \_ LPWSTR   |
| **PKEY \_ ParentalRatingReason**                                           | [System. ParentalRatingReason](../properties/props-system-parentalratingreason.md)                   | 指派的家長評等的原因。                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 評等**                                                         | [系統評分](../properties/props-system-rating.md)                                               | 使用者評等。                                                                                                                                                                                              | VT \_ UI4      |
| **PKEY \_ ThumbnailStream**                                                | [System. ThumbnailStream](../properties/props-system-thumbnailstream.md)                             | 縮圖影像。                                                                                                                                                                                          | VT \_ 資料流程   |
| **PKEY \_ 標題**                                                          | [System.Title](../properties/props-system-title.md)                                                 | 標題。                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ 視頻 \_ 壓縮**                                             | [系統 Video. 壓縮](../properties/props-system-video-compression.md)                         |  ([**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 的影片子類型) 以字串表示。                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 影片 \_ 總監**                                                | [System.servicemodel](../properties/props-system-video-director.md)                               | 導演。                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ 影片 \_ EncodingBitrate**                                         | [EncodingBitrate](../properties/props-system-video-encodingbitrate.md)                 | 平均影片位速率（以每秒位數為單位）。                                                                                                                                                               | VT \_ UI4      |
| **PKEY \_ 影片 \_ FourCC**                                                  | [FourCC](../properties/props-system-video-fourcc.md)                                   | 影片編碼格式的 **FOURCC** 。 只有當影片子類型可以表示為 **FOURCC** 值時才適用。                                                                                    | VT \_ UI4      |
| **PKEY \_ 影片 \_ FrameHeight**                                             | [FrameHeight](../properties/props-system-video-frameheight.md)                         | 影片框架高度。                                                                                                                                                                                       | VT \_ UI4      |
| **PKEY \_ 影片的 \_ 畫面播放速率**                                               | [System.string](../properties/props-system-video-framerate.md)                             | 影片畫面播放速率，以每秒畫面數×1000表示。                                                                                                                                                  | VT \_ UI4      |
| **PKEY \_ 影片 \_ FrameWidth**                                              | [FrameWidth](../properties/props-system-video-framewidth.md)                           | 影片畫面格寬度。                                                                                                                                                                                        | VT \_ UI4      |
| **PKEY \_ 影片 \_ HorizontalAspectRatio**                                   | [HorizontalAspectRatio](../properties/props-system-video-horizontalaspectratio.md)     | 圖元外觀比例的水準元件。  (相當於媒體類型中的 [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性的分子。 )           | VT \_ UI4      |
| **PKEY \_ 影片 \_ IsStereo**                                                | [IsStereo](/previous-versions//mt744507(v=vs.85))                                     | 指出影片資料流程是否包含身歷聲影片內容。                                                                                                                                         | VT \_ BOOL     |
| **PKEY \_ 影片 \_ StreamNumber**                                            | [StreamNumber](../properties/props-system-video-streamnumber.md)                       | 影片資料流程的識別碼。                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ 影片 \_ TotalBitrate**                                            | [TotalBitrate](../properties/props-system-video-totalbitrate.md)                       | 所有影片和音訊串流的總數據速率（以每秒位數為單位）。  (僅適用于具有至少一個影片串流的檔案。 )                                                                               | VT \_ UI4      |
| **PKEY \_ 影片 \_ VerticalAspectRatio**                                     | [VerticalAspectRatio](../properties/props-system-video-verticalaspectratio.md)         | 圖元外觀比例的垂直元件。  (相當於媒體類型中的 [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) 屬性的分母。 )           | VT \_ UI4      |



 

## <a name="media-sharing-properties"></a>媒體共用屬性

若要使媒體檔案與媒體共用功能相容，屬性處理常式應該公開下列中繼資料屬性。 這些屬性可讓媒體共用服務提供適當的選項，以將內容轉碼成不同的格式或位元速率。

-   [MFPKEY \_ Content \_ DLNA \_ 設定檔 \_ 識別碼](mfpkey-content-dlna-profile-id.md)
-   **PKEY \_ 音訊 \_ ChannelCount**
-   **PKEY \_ 音訊 \_ EncodingBitrate**
-   **PKEY \_ 音訊 \_ 格式**
-   **PKEY \_音訊 \_ SampleRate** (選用) 
-   **PKEY \_音訊 \_ SampleSize** (選用) 
-   **PKEY \_Drm \_** 內容) 所需的 drm IsProtected (
-   **PKEY \_ 媒體 \_ 持續時間**
-   **PKEY \_ 視頻 \_ 壓縮**
-   **PKEY \_ 影片 \_ EncodingBitrate**
-   **PKEY \_ 影片 \_ FOURCC**
-   **PKEY \_ 影片 \_ FrameHeight**
-   **PKEY \_ (選用) 的影片 \_ 幀率**
-   **PKEY \_ 影片 \_ FrameWidth**
-   **PKEY \_ 影片 \_ TotalBitrate**

如果使用 DRM 保護內容，則需要 **PKEY \_ DRM \_ IsProtected** 屬性。 否則，這個屬性是選擇性的。

**PKEY \_ 音訊 \_ SampleRate**、 **PKEY \_ audio \_ SampleSize** 和 **PKEY \_ Video \_ 幀** 的屬性都是選擇性的。 媒體共用服務會公開這些服務（如果有的話）。

**PKEY \_ 音訊 _ 群組中的屬性 \_ \* *僅適用于具有音訊串流的檔案，而 _* PKEY \_ 影片 \_ \* 群組中的屬性** 僅適用于具有影片串流的檔案。

## <a name="windows-media-format-sdk-mappings"></a>Windows Media Format SDK 對應

ASF 媒體來源會將下列屬性索引鍵對應至 ASF 標頭屬性。 在某些情況下，Shell 屬性與格式 SDK 屬性之間的資料類型不同。



| PROPERTYKEY                              | 格式 SDK 屬性                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **PKEY \_ 音訊 \_ IsVariableBitRate**       | [**IsVBR**](../wmformat/isvbr.md)                                           |
| **PKEY \_ 音訊 \_ PeakValue**               | [**PeakValue**](../wmformat/peakvalue.md)                                   |
| **PKEY \_ 作者**                         | [**作者**](../wmformat/author.md)                                         |
| **PKEY \_ 批註**                        | [**描述**](../wmformat/description.md)                               |
| **PKEY \_ 著作權**                      | [**著作權**](../wmformat/copyright.md)                                   |
| **PKEY \_ DRM \_ IsProtected**               | [**\_受保護**](../wmformat/is-protected.md)                            |
| **PKEY \_ 關鍵字**                       | [**WM/類別**](../wmformat/wm-category.md)                               |
| **PKEY \_ 語言**                       | [**WM/語言**](../wmformat/wm-language.md)                               |
| **PKEY \_ 媒體 \_ AuthorUrl**               | [**WM/AuthorURL**](../wmformat/wm-authorurl.md)                             |
| **PKEY \_ 媒體 \_ AverageLevel**            | [**AverageLevel**](../wmformat/averagelevel.md)                             |
| **PKEY \_ 媒體 \_ ClassPrimaryID**          | [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md)              |
| **PKEY \_ 媒體 \_ ClassSecondaryID**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **PKEY \_ 媒體 \_ CollectionGroupID**       | [**WM/WMCollectionGroupID**](../wmformat/wm-wmcollectiongroupid.md)         |
| **PKEY \_ 媒體 \_ CollectionID**            | [**WM/WMCollectionID**](../wmformat/wm-wmcollectionid.md)                   |
| **PKEY \_ 媒體 \_ ContentDistributor**      | [**WM/ContentDistributor**](../wmformat/wm-contentdistributor.md)           |
| **PKEY \_ 媒體 \_ ContentID**               | [**WM/WMContentID**](../wmformat/wm-wmcontentid.md)                         |
| **PKEY \_ 媒體 \_ DateEncoded**             | [**WM/EncodingTime**](../wmformat/wm-encodingtime.md)                       |
| **PKEY \_ 媒體 \_ DateReleased**            | [**WM/OriginalReleaseTime**](../wmformat/wm-originalreleasetime.md)         |
| **PKEY \_ 媒體 \_ DVDID**                   | [**WM/DVDID**](../wmformat/wm-dvdid.md)                                     |
| **PKEY \_ 媒體 \_ EncodedBy**               | [**WM/EncodedBy**](../wmformat/wm-encodedby.md)                             |
| **PKEY \_ 媒體 \_ EncodingSettings**        | [**WM/EncodingSettings**](../wmformat/wm-encodingsettings.md)               |
| **PKEY \_ 媒體 \_ MCDI**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **PKEY \_ 媒體 \_ MetadataContentProvider** | [**WM/提供者**](../wmformat/wm-provider.md)                               |
| **PKEY \_ 媒體 \_ 生產者**                | [**WM/生產者**](../wmformat/wm-producer.md)                               |
| **PKEY \_ 媒體 \_ PromotionUrl**            | [**WM/PromotionURL**](../wmformat/wm-promotionurl.md)                       |
| **PKEY \_ 媒體 \_ ProviderRating**          | [**WM/ProviderRating**](../wmformat/wm-providerrating.md)                   |
| **PKEY \_ 媒體 \_ ProviderStyle**           | [**WM/ProviderStyle**](../wmformat/wm-providerstyle.md)                     |
| **PKEY \_ 媒體 \_ 發行者**               | [**WM/發行者**](../wmformat/wm-publisher.md)                             |
| **PKEY \_ 媒體 \_ 副標題**                | [**WM/SubTitleDescription**](../wmformat/wm-subtitledescription.md)         |
| **PKEY \_ 媒體 \_ UniqueFileIdentifier**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **PKEY \_ 媒體 \_ 寫入器**                  | [**WM/Writer**](../wmformat/wm-writer.md)                                   |
| **PKEY \_ Media \_ Year**                    | [**WM/年**](../wmformat/wm-year.md)                                       |
| **PKEY \_ 音樂 \_ AlbumArtist**             | [**WM/AlbumArtist**](../wmformat/wm-albumartist.md)                         |
| **PKEY \_ 音樂 \_ AlbumTitle**              | [**WM/AlbumTitle**](../wmformat/wm-albumtitle.md)                           |
| **PKEY \_ 音樂 \_ 演出者**                  | [**作者**](../wmformat/author.md)                                         |
| **PKEY \_ 音樂 \_ BeatsPerMinute**          | [**WM/BeatsPerMinute**](../wmformat/wm-beatsperminute.md)                   |
| **PKEY \_ 音樂 \_ 編輯器**                | [**WM/編輯器**](../wmformat/wm-composer.md)                               |
| **PKEY \_ 音樂 \_ 導體**               | [**WM/導體**](../wmformat/wm-conductor.md)                             |
| **PKEY \_ 音樂 \_ ContentGroupDescription** | [**WM/ContentGroupDescription**](../wmformat/wm-contentgroupdescription.md) |
| **PKEY \_ 音樂 \_ 類型**                   | [**WM/內容類型**](../wmformat/wm-genre.md)                                     |
| **PKEY \_ 音樂 \_ InitialKey**              | [**WM/InitialKey**](../wmformat/wm-initialkey.md)                           |
| **PKEY \_ 音樂 \_ IsCompilation**           | **WM/IsCompilation**                                                  |
| **PKEY \_ 音樂 \_ 歌詞**                  | [**WM/歌詞**](../wmformat/wm-lyrics.md)                                   |
| **PKEY \_ 音樂的 \_ 情緒**                    | [**WM/情緒**](../wmformat/wm-mood.md)                                       |
| **PKEY \_ 音樂 \_ PartOfSet**               | [**WM/PartOfSet**](../wmformat/wm-partofset.md)                             |
| **PKEY \_ 音樂 \_ 期間**                  | [**WM/句號**](../wmformat/wm-period.md)                                   |
| **PKEY \_ 音樂 \_ TrackNumber**             | [**WM/TrackNumber**](../wmformat/wm-tracknumber.md)                         |
| **PKEY \_ ParentalRating**                 | [**WM/ParentalRating**](../wmformat/wm-parentalrating.md)                   |
| **PKEY \_ ParentalRatingReason**           | [**WM/ParentalRatingReason**](../wmformat/wm-parentalratingreason.md)       |
| **PKEY \_ 評等**                         | [**WM/SharedUserRating**](../wmformat/wm-shareduserrating.md)               |
| **PKEY \_ ThumbnailStream**                | [**WM/圖片**](../wmformat/wmpicture.md)                       |
| **PKEY \_ 標題**                          | [**標題**](../wmformat/title.md)                                           |
| **PKEY \_ 影片 \_ 總監**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體中繼資料](media-metadata.md)
</dt> <dt>

[Shell 中繼資料提供者](shell-metadata-providers.md)
</dt> </dl>

 

 
