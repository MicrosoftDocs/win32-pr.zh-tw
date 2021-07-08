---
description: 屬性系統包含名為 system.string 的屬性，它會根據副檔名將專案分割成類型，以及使用者可以輕鬆地識別。
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: 使用種類名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481873"
---
# <a name="using-kind-names"></a>使用種類名稱

屬性系統包含名為的屬性 `System.Kind` ，它會根據副檔名將專案分割成類型，以及使用者可以輕鬆地識別。

本主題的組織方式如下：

-   [關於 System.object 屬性](#about-the-systemkind-property)
-   [種類值階層和註冊](#kind-value-hierarchy-and-registration)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-the-systemkind-property"></a>關於 System.object 屬性

種類是在 Windows Vista 中引進，以表達更容易使用的檔案類型概念。 `System.Kind`屬性會將專案分割成類型，並提供終端使用者可以識別的種類名稱，例如檔、音樂、圖片等等。 因此，種類名稱就稱為「使用者易記」。 因為 `System.Kind` 相同檔案類型的專案會將屬性設定為相同的值，並將具有類似特性的專案與通用屬性產生關聯，所以系統和使用者可以針對整個群組進行動作。 例如， `System.Kind` 屬性可用來限制搜尋特定種類的專案、顯示內容視圖中專案的最相關屬性，或將類似的專案群組在一起。

因為 Kind 是多重值字串屬性，所以您可以有 `audio;video` 或種類的 `link;document` 值。 `System.Kind`值是字串值的排序清單。 在某些情況下，該清單中可能只有一個元素。 在其他情況下，專案可以屬於一個以上的類型。 如需屬於一種以上類型的專案範例，請參閱本主題中的登錄機碼範例。 字串值來自一組預先定義的已知值。 使用不區分大小寫和不區分地區設定的字串比較函式來比較值。 這些字串並不會當地語系化。

某些種類的名稱已與屬性和配置模式相關聯。 例如，與相關聯的專案 `Kind.Picture` 以及與相關聯的專案， `Kind.Document` 即使它們都在相同的視圖中，也會顯示不同的屬性，因為已與這兩種類型的名稱相關聯的屬性和配置模式。 每個專案種類都可以與四種獨特的版面配置模式之一建立關聯，以定義每個專案和其配置所顯示的屬性數目。 如需詳細資訊，請參閱以 [檔案類型或種類關聯為基礎的內容視圖](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))。

## <a name="kind-value-hierarchy-and-registration"></a>種類值階層和註冊

`Kind`值必須代表下列清單中的其中一個值。

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

屬性處理常式可以 `System.Kind` 透過登錄以靜態方式宣告其屬性，也可以透過其程式碼以動態方式提供值，就像使用標準屬性一樣。

若要以靜態 `Kind` 方式定義屬性，會在 **KindMap** 登錄機碼底下加入 **REG \_ SZ** 值專案，如下列範例所示。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

請注意， `Kind` 可以是單一值或分號分隔字串中的多個值。 提供多個值時， `Kind` 會先列出最特定的值，並指定下列最小的值。 在此範例中，會先命名 Contact，因為它的階層比通訊更明確。 假設為值 **專案** ，不應該提供明確。

## <a name="additional-resources"></a>其他資源

-   如需屬性的參考檔， [請參閱](./props-system-kind.md) [KindText](./props-system-kindtext.md)。
-   如需建立新的或使用現有檔案類型的詳細資訊，請參閱 [檔案類型](../shell/fa-file-types.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解屬性處理常式](./building-property-handlers-properties.md)
</dt> <dt>

[使用屬性清單](./building-property-handlers-property-lists.md)
</dt> <dt>

[初始化屬性處理常式](./building-property-handlers-property-handlers.md)
</dt> <dt>

[註冊和散發屬性處理常式](./prophand-reg-dist.md)
</dt> <dt>

[屬性處理常式的最佳作法和常見問題](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
