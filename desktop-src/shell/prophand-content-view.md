---
description: 本主題說明 Windows 檔案總管中稱為內容視圖的新視圖，它會顯示每個專案最相關的內容。
title: 依檔案類型或種類的內容視圖
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 83f70649bd0eb022bde9cc4a8c69e0df162fe2551268f611390bae835409e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858709"
---
# <a name="content-view-by-file-type-or-kind"></a>依檔案類型或種類的內容視圖

本主題說明 Windows 檔案總管中稱為內容視圖的新視圖，它會顯示每個專案最相關的內容。 專案可以使用一組登錄機碼來定義屬性清單，以及 Shell 用於內容視圖的版面配置。 Shell 會使用專案的 [關聯陣列](fa-perceivedtypes.md)來抓取登錄機碼。

## <a name="how-does-the-content-view-work"></a>內容視圖的運作方式為何？

在 Windows 7 和更新版本中，內容視圖會使用調整大小邏輯來放置視窗大小減少時的屬性，以確保最重要的屬性仍然具有可清楚讀取的空間。 下列螢幕擷取畫面說明包含音樂、圖片和檔的搜尋結果內容視圖。

![包含音樂、圖片和檔的搜尋結果內容視圖](images/content-view/contentviewsearchresults.png)

某些 Shell 資料來源預設會使用內容視圖，但使用者可以按一下 [Windows 檔案總管] 中的 [ **view Control** ] 按鈕，以選取內容視圖。 Shell 資料來源會擴充 Shell 命名空間，並公開資料存放區中的專案。 您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。

## <a name="how-to-implement-the-content-view"></a>如何執行內容視圖

註冊新的 [檔案類型](fa-file-types.md) 或 [通訊協定處理常式](../search/-search-3x-wds-extidx-prot-implementing.md)時，您可以使用兩種不同方法的其中一種來利用內容視圖。 您可以使用現有的屬性集和版面配置模式，也可以建立自己的組合。

您可以使用登錄專案，將您的檔案類型或專案與預先定義的 [種類](../properties/building-property-handlers-user-friendly-kind-names.md)產生關聯，這是您可以將它視為內容類別別的屬性。 藉由將您的檔案類型或專案與這些種類的某些專案產生關聯，您就可以自動繼承該種類的內容視圖配置模式和屬性清單。 Windows 定義下列種類的內容視圖配置模式和屬性清單：檔、電子郵件、資料夾、音樂、圖片和一般。 建議您這樣的關聯類型。 它可讓您提供使用者預期類似專案的一致體驗。

如需詳細資訊，請參閱 [檔](fa-file-types.md) 類型和 [種類名稱](../properties/building-property-handlers-user-friendly-kind-names.md) ，以及 [如何針對檔案類型或專案註冊屬性的唯一內容集和配置模式](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md)。

## <a name="additional-resources"></a>其他資源

-   如需屬性參考 [檔，請參閱 system.string](../properties/props-system-kind.md)和 [system. KindText](../properties/props-system-kindtext.md)。
-   如需 PropList 參考檔，請參閱 [PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)和 [PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 
