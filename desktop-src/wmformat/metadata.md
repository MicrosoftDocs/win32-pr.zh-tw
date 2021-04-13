---
title: 中繼資料
description: 基於這個 SDK 的目的，中繼資料是描述 ASF 檔案或檔案內容的資訊。
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK，中繼資料總覽
- Advanced Systems Format (ASF) ，中繼資料總覽
- ASF (Advanced Systems Format) ，中繼資料總覽
- 中繼資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311252"
---
# <a name="metadata"></a>中繼資料

基於這個 SDK 的目的，中繼資料是描述 ASF 檔案或檔案內容的資訊。 ASF 檔案的標頭區段包含與該檔案相關聯的所有中繼資料。 ASF 檔案中中繼資料的個別專案稱為屬性。 每個屬性都有名稱和值。 在本檔中，全域常數用來識別屬性。 例如，ASF 檔案的標題會儲存在 **g \_ wszWMTitle** 屬性中。

Windows Media Format SDK 中定義了數個屬性，可處理最常見的中繼資料需求。 此外，您還可以建立自己的屬性。 不過，您應該在命名自訂屬性時小心，因為其他應用程式開發人員可以使用相同的名稱，而且可能會發生衝突。

有些屬性是由 SDK 設定，無法手動變更。 例如，當您為 ASF 檔案編制索引時，SDK 會設定 **g \_ wszWMSeekable** 屬性，以顯示現在可以從任何指定的點讀取該檔案。

其他屬性則是單純的資訊，必須手動設定。 例如，如果您想要追蹤檔案的作者，您應該設定 **g \_ wszWMAuthor**。

Windows Media Format SDK 提供適用于整個檔案的屬性，以及適用于個別資料流程的屬性支援。

您可以使用 Windows Media Format SDK 來編輯 MP3 檔案中的中繼資料，不過，您應該一律在 MP3 檔中使用 ID3 相容的屬性，以維持與其他 MP3 操作程式的相容性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](concepts.md)
</dt> <dt>

[**中繼資料編輯器物件**](metadata-editor-object.md)
</dt> <dt>

[**中繼資料功能**](metadata-features.md)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




