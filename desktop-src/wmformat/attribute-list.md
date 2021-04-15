---
title: 屬性清單
description: 屬性清單
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507923"
---
# <a name="attribute-list"></a>屬性清單

下表依字母順序顯示此 SDK 中包含的預先定義屬性。 每個屬性都有名稱、全域識別碼，以及 [**WMT \_ ATTR \_ DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) 列舉的適當成員所定義的資料類型。 某些屬性不會使用簡單的資料類型，或會根據結構來格式化。 這些屬性的專案會在 [資料類型] 資料行中列出結構名稱，此資料類型是用來設定括弧中的值。

> [!Note]  
> 請參閱 [Drm 屬性清單](drm-attribute-list.md) ，以取得所有 DRM 相關屬性的表格。

 

當您使用這些屬性進行程式設計時，您應該使用全域識別碼，而不是使用名稱做為字串常值。 藉由使用全域識別碼，任何印刷錯誤都會在編譯時期產生錯誤。



| 屬性名稱                                                                       | 全域識別碼                             | 資料類型                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **WMT \_ 類型 \_ 二進位**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **WMT \_ 類型 \_ DWORD**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **WMT \_ 類型 \_ DWORD**                                 |
| [**作者**](author.md)                                                             | g \_ wszWMAuthor                                | **WMT \_ 類型 \_ 字串**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **WMT \_ 類型 \_ DWORD**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **WMT \_ 類型 \_ 二進位**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **WMT \_ 類型 \_ DWORD**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **WMT \_ 類型 \_ 字串**                                |
| [**位元速率**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **WMT \_ 類型 \_ DWORD**                                 |
| [**廣播**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **WMT \_ 類型 \_ BOOL**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **WMT \_ 類型 \_ DWORD**                                 |
| [**可以 \_ 向前跳過 \_**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **WMT \_ 類型 \_ BOOL**                                  |
| [**可以 \_ 向前跳過 \_**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **WMT \_ 類型 \_ BOOL**                                  |
| [**著作權**](copyright.md)                                                       | g \_ wszWMCopyright                             | **WMT \_ 類型 \_ 字串**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **WMT \_ 類型 \_ 字串**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **WMT \_ 類型 \_ DWORD**                                 |
| [**描述**](description.md)                                                   | g \_ wszWMDescription                           | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ ContentID**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentID                        | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ ContentDistributor**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ ContentID**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentID             | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)                                 | g \_ wszWMDRM \_ DRMHeader \_ KeyID                 | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader \_ SubscriptionContentID**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ DRMHeader**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ KeyID**](drm-keyid.md)                                                      | g \_ wszWMDRM \_ KeyID                            | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ LicenseID**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **WMT \_ 類型 \_ 字串**                                |
| [**DRM \_ SourceID**](drm-sourceid.md)                                                | g \_ wszWMDRM \_ SourceID                         | **WMT \_ 類型 \_ DWORD**                                 |
| [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **WMT \_ 類型 \_ 字串**                                |
| [**持續時間**](duration.md)                                                         | g \_ wszWMDuration                              | **WMT \_ 類型 \_ QWORD**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszWMFileSize                              | **WMT \_ 類型 \_ QWORD**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **WMT \_ 類型 \_ BOOL**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **WMT \_ 類型 \_ BOOL**                                  |
| [**\_受保護**](is-protected.md)                                                | g \_ wszWMProtected                             | **WMT \_ 類型 \_ BOOL**                                  |
| [**\_受信任**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **WMT \_ 類型 \_ BOOL**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszISAN                                    | **WMT \_ 類型 \_ 字串**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **WMT \_ 類型 \_ BOOL**                                  |
| [**.NSC \_ 位址**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **WMT \_ 類型 \_ 字串**                                |
| [**.NSC \_ 描述**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **WMT \_ 類型 \_ 字串**                                |
| [**.NSC \_ 電子郵件**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **WMT \_ 類型 \_ 字串**                                |
| [**.NSC \_ 名稱**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **WMT \_ 類型 \_ 字串**                                |
| [**.NSC \_ 電話**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **WMT \_ 類型 \_ 字串**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **WMT \_ 類型 \_ QWORD**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **WMT \_ 類型 \_ DWORD**                                 |
| [**PeakValue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **WMT \_ 類型 \_ DWORD**                                 |
| [**分級**](rating.md)                                                             | g \_ wszWMRating                                | **WMT \_ 類型 \_ 字串**                                |
| [**查找**](seekable.md)                                                         | g \_ wszWMSeekable                              | **WMT \_ 類型 \_ BOOL**                                  |
| [**簽名 \_ 名稱**](signature-name.md)                                            | g \_ wszWMSignature \_ 名稱                       | **WMT \_ 類型 \_ 字串**                                |
| [**Stridable**](stridable.md)                                                       | g \_ wszWMStridable                             | **WMT \_ 類型 \_ BOOL**                                  |
| [**標題**](title.md)                                                               | g \_ wszWMTitle                                 | **WMT \_ 類型 \_ 字串**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMAlbumArtist                           | **WMT \_ 類型 \_ 字串**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMAlbumCoverURL                         | **WMT \_ 類型 \_ 字串**                                |
| [**WM/AlbumTitle**](wm-albumtitle.md)                                               | g \_ wszWMAlbumTitle                            | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **WMT \_ 類型 \_ QWORD**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **WMT \_ 類型 \_ QWORD**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **WMT \_ 類型 \_ 字串**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/類別**](wm-category.md)                                                   | g \_ wszWMCategory                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/編解碼器**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **WMT \_ 類型 \_ 字串**                                |
| [**WM/編輯器**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/導體**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ (\_** **WMT \_ 類型 \_ 二進位**) 的儲存格式     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **WMT \_ 類型 \_ 字串**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszWMDirector                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **WMT \_ 類型 \_ 字串**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **WMT \_ 類型 \_ 字串**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **WMT \_ 類型 \_ 字串**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**WMT \_ 類型 \_ QWORD**)                   |
| [**WM/內容類型**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **WMT \_ 類型 \_ 字串**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **WMT \_ 類型 \_ 字串**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/語言**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/歌詞**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **WMT \_ 類型 \_ 字串**                                |
| [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ 內容                  | **WM \_內容 \_ 歌詞** (**WMT \_ 類型 \_ 二進位**)  |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **WMT \_ 類型 \_ 二進位**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **WMT \_ 類型 \_ GUID**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **WMT \_ 類型 \_ GUID**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **WMT \_ 類型 \_ 字串**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **WMT \_ 類型 \_ 字串**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **WMT \_ 類型 \_ 字串**                                |
| [**WM/情緒**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalAlbumTitle                    | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **WMT \_ 類型 \_ 字串**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/句號**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **WMT \_ 類型 \_ 字串**                                |
| [**WM/圖片**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_圖片** (**WMT \_ 類型 \_ BINARY**)               |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **WMT \_ 類型 \_ 字串**                                |
| [**WM/生產者**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **WMT \_ 類型 \_ 字串**                                |
| [**WM/Set-protectiontype**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/提供者**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **WMT \_ 類型 \_ 字串**                                |
| [**WM/發行者**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | g \_ wszWMRadioStationName                      | **WMT \_ 類型 \_ 字串**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWMRadioStationOwner                     | **WMT \_ 類型 \_ 字串**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_資料流程 \_ 類型 \_ 資訊** (**WMT \_ 類型 \_ BINARY**)    |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **WMT \_ 類型 \_ 字串**                                |
| [**WM/子標題**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **WMT \_ 類型 \_ 字串**                                |
| [**WM/Text**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_使用者 \_ 文字** (**WMT \_ 類型 \_ 二進位**)            |
| [**WM/工具**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **WMT \_ 類型 \_ 字串**                                |
| [**WM/ToolVersion**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **WMT \_ 類型 \_ 字串**                                |
| [**WM/曲目**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **WMT \_ 類型 \_ 字串**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **WMT \_ 類型 \_ 字串**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **WMT \_ 類型 \_ 字串**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_使用者 \_ WEB \_ URL** (**WMT \_ 類型 \_ 二進位**)        |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **WMT \_ 類型 \_ BOOL**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **WMT \_ 類型 \_ DWORD**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **WMT \_ 類型 \_ GUID**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **WMT \_ 類型 \_ GUID**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **WMT \_ 類型 \_ GUID**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **WMT \_ 類型 \_ 字串**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **WMT \_ 類型 \_ 字串**                                |
| [**WM/Writer**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **WMT \_ 類型 \_ 字串**                                |
| [**WM/年**](wm-year.md)                                                           | g \_ wszWMYear                                  | **WMT \_ 類型 \_ 字串**                                |



 

## <a name="remarks"></a>備註

以下是以屬性定義的常數。 每一個都代表特定類型的屬性數目。 您不需要針對應用程式中的任何值使用這些值。



| 常數                 | 值 |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 