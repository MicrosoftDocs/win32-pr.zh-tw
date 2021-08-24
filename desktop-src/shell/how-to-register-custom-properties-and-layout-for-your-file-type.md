---
description: 當您瞭解搜尋結果模式、瀏覽模式和版面配置模式之後，就可以為您的檔案類型註冊自訂屬性清單。若要為您的檔案類型註冊自訂屬性清單和配置模式，請遵循下列步驟。
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: 如何註冊您的檔案類型的自訂屬性和版面配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9388965a781d4104ae13de689b72208a8b69e213a758c9b34552c03bb938453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714898"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>如何註冊您的檔案類型的自訂屬性和版面配置

當您瞭解搜尋結果模式、瀏覽模式和版面配置模式之後，就可以為您的檔案類型註冊自訂屬性清單。

若要為您的檔案類型註冊自訂屬性清單和配置模式，請遵循下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

從四種版面配置模式中選擇： Alpha、Beta、Gamma 或 Delta。

### <a name="step-2"></a>步驟 2:

請考慮下列格式化規則，這同樣適用于全部四種版面配置模式：

-   屬性1一律會以較大的字型大小顯示。 大型字型大小通常用於專案名稱，但也可以用於錨點或其他專案屬性。
-   屬性4適用于 Alpha、Beta 和 Gamma 版面配置模式中的摘錄。 這個屬性會在這些模式中配置更多空間，並以灰色字型色彩顯示，而不像其他屬性一樣黑色，以協助它脫穎而出。
-   下方的圖元測量是以相對圖元為單位，而大小則包含屬性左邊的圖示/縮圖，以及圖示/縮圖和選取矩形之間的間距。
-   大部分屬性都有最小的顯示大小。 因此，如果沒有足夠的空間可供特定的視圖大小使用，它們就不會出現。 大小下限通常是100圖元寬。
-   每個配置模式都會定義每個資料列中的資料列數目和屬性數目。

### <a name="step-3"></a>步驟 3：

決定您想要在版面配置中顯示哪些屬性，以及要在每個位置顯示哪個屬性。 當您決定要在版面配置中的每個位置顯示哪一個屬性時，請考慮屬性的一般長度、對使用者的重要性，以及當視窗大小太小而無法包含所有屬性時是否應該卸載。

### <a name="step-4"></a>步驟 4：

為您的檔案類型或專案類型，在此範例中的檔案類型或專案 (的 ProgID 登錄機碼底下加入下列索引鍵，以註冊配置模式和屬性清單，) 的 [xyz] 檔案類型。

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>步驟 5：

請觀察下列用於註冊屬性的格式化指導方針：

-   每個註冊的開頭為 `prop:`
-   每個屬性都需要完整的屬性名稱。
-   屬性以分號分隔，而且沒有空格。
-   屬性會依所選版面配置模式所定義的順序顯示。
-   `~` 指出不應該顯示內容標籤。
-   `~System.LayoutPattern.PlaceHolder` 如果您想要將配置模式所指定的屬性保留空白，則應該使用。

下列範例登錄機碼說明這些格式設定指導方針。

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

 (ContentViewModeForBrowse) 的可能值包括下列各項： `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



