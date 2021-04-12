---
description: 檔案關聯會定義 Shell 如何處理系統上的檔案類型。
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: 檔案關聯的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192705"
---
# <a name="how-file-associations-work"></a>檔案關聯的運作方式

檔案關聯會定義 Shell 如何處理系統上的 [檔案類型](fa-file-types.md) 。

本主題的組織方式如下：

-   [關於檔案關聯](#about-file-associations)
-   [當您應執行或修改檔案關聯時](#when-you-should-implement-or-modify-file-associations)
-   [檔案關聯的運作方式](#how-file-associations-work)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-file-associations"></a>關於檔案關聯

檔案關聯控制下列功能：

-   當使用者按兩下檔案時，會啟動哪個應用程式。
-   預設會顯示檔案的圖示。
-   在 Windows 檔案總管中查看時，檔案類型的顯示方式。
-   檔案的快捷方式功能表中會出現哪些命令。
-   其他 UI 功能，例如工具提示、磚資訊和詳細資料窗格。

應用程式開發人員可以使用檔案關聯來控制 Shell 處理自訂檔案類型的方式，或將應用程式與現有的檔案類型產生關聯。 例如，安裝應用程式時，應用程式可以檢查現有的檔案關聯是否存在，並建立或覆寫這些檔案關聯。

使用者可以控制檔案關聯的某些層面，以自訂 Shell 如何使用 [ **開啟** 檔案] UI 或編輯登錄來處理檔案類型。

在以下螢幕擷取畫面所示的 [Windows 檔案總管] 視窗中，Shell 會根據與檔案類型相關聯的圖示，為每個檔案顯示不同的圖示。 如果使用者按兩下檔案 **範例點陣圖影像**，則 Shell 會啟動油漆，並用它來開啟檔案，因為在這個系統上，油漆與 .bmp 檔案相關聯。 人們可以使用檔案關聯來控制這些動作。

![檔案關聯在實務上的運作方式圖例](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>當您應執行或修改檔案關聯時

應用程式可基於各種用途使用檔案：某些檔案是由應用程式專用使用，而且通常不會由使用者存取，而其他檔案則由使用者建立，且通常會從 Shell 開啟、搜尋和查看。

除非您的自訂檔案類型是由應用程式獨佔使用，否則您應該為它執行檔案關聯。 一般來說，如果您預期使用者會以任何方式直接與這些檔案互動，請針對您的自訂檔案類型來執行檔案關聯。 這包括使用 Shell 來流覽和開啟檔案、搜尋檔案的內容或屬性，以及預覽檔案。

如果您的應用程式正在處理現有的檔案類型，除非您想要修改 Shell 處理此類型之所有檔案的方式，否則請勿修改檔案關聯。

## <a name="how-file-associations-work"></a>檔案關聯的運作方式

檔案會在 Shell 中公開為 Shell 專案。 若要控制檔案關聯，應用程式開發人員可以在檔案類型與處理常式之間註冊對應， (COM 物件，這些物件會提供檔案類型之 Shell 專案) 的功能。 當 Shell 需要查詢檔案類型的檔案關聯時，它會建立包含檔案類型關聯的登錄機碼陣列，並檢查這些機碼是否有適當的檔案關聯可供使用。

## <a name="additional-resources"></a>其他資源

-   如需檔案關聯的概念背景，請參閱 [動詞和檔案關聯的總覽](fa-verbs.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
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

 

 



