---
title: 程式庫位置常數
description: 程式庫位置常數
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player 線上商店、程式庫位置常數
- 線上商店、程式庫位置常數
- 輸入1個線上商店、程式庫位置常數
- Windows Media Player 線上商店、位置
- 線上商店、位置
- 輸入1個線上商店、位置
- Windows Media Player 程式庫，位置常數
- 程式庫，位置常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cbb297831acce9724988309880390cdcbe1894
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374796"
---
# <a name="library-location-constants"></a>程式庫位置常數

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

程式庫位置常數是在 contentpartner 中定義的全域字串變數。 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)和[IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)介面的某些方法和[外部](external-object-for-type-1-online-stores.md)物件的特定方法會使用這些方法。 這些常數用來表示下列類型。

-   程式庫位置類型：這是 Windows Media Player 所顯示的程式庫檢視類型。 例如，播放程式可能會顯示特定專輯 (g \_ szCPAlbumID) 或 (g szAllCPGenreIDs) 的所有內容視圖 \_ 。
-   選取的專案類型：這是在程式庫視圖中選取的專案類型。 例如，使用者可能會 \_ 在所有專輯的視圖中選取特定的專輯 (g szCPAlbumID) 。
-   清單類型：這是要從內容合作夥伴外掛程式要求的清單類型。 例如，Windows Media Player 可能會要求外掛程式提供與特定播放清單相關聯的專案清單 (g \_ szCPListID) 。
-   清單專案類型：從內容合作夥伴外掛程式要求的個別清單專案類型。 例如，Windows Media Player 可能會要求外掛程式在 \_ 特定播放清單中提供 (g szCPTrackID) 的曲目清單。

下表提供每個常數的名稱和值，以及程式庫位置或類型的簡短描述。 在使用 contentpartner .h 標頭檔編譯的 C 或 c + + 程式碼中，您可以使用常數的名稱或值。 最好使用名稱，因為編譯器會偵測到拼寫錯誤。 例如，在腳本 (例如，呼叫 [外部](external-object-for-type-1-online-stores.md) 物件) 的方法時，您無法使用常數的名稱;您必須使用此值。



| Name                              | 值                        | 位置或類型                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | Unknownlocation.xsd              | 不是專輯也不是播放清單的一組曲目。 在罕見的情況下，Windows Media Player 也會使用這個常數，因為它無法判斷有效的位置。 |
| g \_ szRootLocation                 | RootLocation                 | 程式庫樹狀檢視控制項中的最上層節點                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | 目前線上商店的飛出視窗功能表                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | 所有線上商店                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | 個別清單                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | 所有清單                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | 個別的追蹤                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | 所有追蹤                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | 個人演出者                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | 所有演出者                                                                                                                                                        |
| g \_ szCPAlbumID                    | CPAlbumID                    | 個別專輯                                                                                                                                                |
| g \_ szAllCPAlbumIDs                | AllCPAlbumIDs                | 所有專輯                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | 個別的類型                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | 所有內容                                                                                                                                                         |
| g \_ szCPAlbumSubGenreID            | CPAlbumSubGenreID            | 個別 subgenre                                                                                                                                             |
| g \_ szAllCPAlbumSubGenreIDs        | AllCPAlbumSubGenreIDs        | 所有 subgenres                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | 發行目錄內容的個人年度                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | 所有目錄內容發行的年度                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | 個別的收音機串流                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | 所有無線電串流                                                                                                                                                  |
| g \_ szAuthor                       | 作者                       | 個人作者                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | 所有作者                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | 個別家長評價                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | 所有家長評等                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | 個別的使用者評等，以星星數來測量                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | 所有使用者評等                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AddToBasket**](external-addtobasket.md)
</dt> <dt>

[**External. 購買**](external-buy.md)
</dt> <dt>

[**ChangeView**](external-changeview.md)
</dt> <dt>

[**ChangeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. 下載**](external-download.md)
</dt> <dt>

[**LibraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner：： InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




