---
description: 察覺的型別是一種檔案類型類別，可讓您將檔案類型識別為 Windows (，而應用程式) 為映射、音訊、檔或其他類型。
title: " (Windows Shell 的認知類型) "
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991862"
---
# <a name="perceived-types-the-windows-shell"></a> (Windows Shell 的認知類型) 

察覺的型別是一種檔案類型類別，可讓您將檔案類型識別為 Windows (，而應用程式) 為映射、音訊、檔或其他類型。 察覺的型別用於多種用途，包括決定資料夾類型，然後用來設定預設的視圖設定。 例如，已將已感知類型映射之檔案的資料夾，指派為縮圖的預設視圖模式。

本主題的組織方式如下：

-   [關於認知類型](#about-perceived-types)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-perceived-types"></a>關於認知類型

定義為 PerceivedType 值的認知類型與檔案類型類似，不同之處在于它們是指檔案格式類型的廣泛分類，而不是特定檔案類型。 例如，影像、文字、音訊和壓縮都是可察覺的類型。 檔案類型 (一般公用檔案類型) 可以被指派一個感知的型別，而且只要有適當的類型，一律會指派一個。 例如，圖像檔案類型 .bmp、.png、.jpg 和 .gif 也是察覺的類型影像。

預設的已知類型如下：

-   資料夾
-   Text
-   Image
-   音訊
-   影片
-   Compressed
-   文件
-   系統
-   Application
-   Gamemedia
-   連絡人

## <a name="additional-resources"></a>其他資源

-   如需如何註冊認知類型的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。
-   如需預設感知類型的清單，請參閱 [**認知**](/windows/win32/api/shtypes/ne-shtypes-perceived) 的列舉。
-   若要根據檔案的副檔名抓取檔案的認知型別，請參閱 [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 



