---
description: 您可以針對檔案類型或專案註冊唯一的內容視圖屬性清單和版面配置模式。
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: 為檔案類型或專案註冊內容視圖集的屬性和版面配置模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104321296"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>如何註冊檔案類型或專案的唯一內容視圖集屬性和配置模式

您可以針對檔案類型或專案註冊唯一的內容視圖屬性清單和版面配置模式。 如果您的檔案類型或專案也與某個種類相關聯，則檔案類型或專案的特定內容視圖註冊將會覆寫種類註冊。 如果這個專案的最重要屬性與相同類型的其他專案不同，這可能會很有用。 如果您沒有將檔案類型或專案與專案種類建立關聯，或直接註冊內容視圖，系統會使用預設的內容查看資訊 (儲存在所有專案的關聯陣列中最後一個元素所參考的登錄機碼中，HKEY \_ 類別 \_ 根目錄 \\ \*) 

註冊檔案類型的自訂屬性清單之前，您應該瞭解搜尋結果模式和瀏覽模式，以及您可以使用的版面配置模式。

## <a name="instructions"></a>指示

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>步驟1：瞭解搜尋結果模式和瀏覽模式

內容視圖需要為一組搜尋結果中的專案定義配置模式和屬性清單的屬性清單 (搜尋結果模式) ，以及流覽至 Shell 位置 (瀏覽模式) 。 您可以使用相同的值來搜尋結果和流覽 `Kind.Music` 。 或者，您也可以定義不同的屬性清單和/或版面配置模式 `Kind.Document` 。

在的案例中 `Kind.Document` ，使用者通常會在檔的文字中搜尋文字。 因此，在搜尋結果中包含更多範例文字，可能是最好的選擇。 下列範例說明的流覽內容視圖 `Kind.Document` 。

![流覽 kind.doc>ument 的內容視圖](images/content-view/browsecontentviewkinddocument.png)

由於使用者很少會在流覽檔時搜尋特定文字，因此優化您所選擇的屬性和版面配置以在螢幕上容納更多搜尋結果，可能是最佳選擇。 下列螢幕擷取畫面說明的搜尋內容視圖 `Kind.Document` 。

### <a name="step-2-understanding-layout-patterns"></a>步驟2：瞭解版面配置模式

有四種配置模式： Alpha、Beta、Gamma 和 Delta。

**Alpha 版面配置**

Alpha 配置模式最適合用於包含摘錄的檔搜尋結果。 它具有下列規格：

-   資料列：4
-   屬性：7
-   當專案具有350圖元或更多水準空間時的 Alpha 配置，如下圖所示。

    ![Alpha 版面配置模式](images/content-view/layout1.png)

-   下圖顯示當專案具有350圖元或更多水準空間時的 Alpha 版面配置。

    ![顯示 Alpha 版面配置範例的圖表](images/content-view/alphaviewmore.png)

-   下圖顯示當專案的水準空間小於350圖元時的 Alpha 版面配置。

    ![顯示 Microsoft Word 中 Alpha 版面配置範例的螢幕擷取畫面。](images/content-view/layout2.png)

-   下圖顯示當專案的水準空間小於350圖元時的 Alpha 版面配置。

    ![Alpha 版面配置範例](images/content-view/alphaviewless.png)

**Beta 版面配置**

Beta 版面配置模式已針對包含摘錄的電子郵件檔搜尋結果進行優化。 它具有下列規格：

-   資料列：4
-   屬性：5
-   當專案具有350圖元或更多水準空間時的 Beta 版面配置，如下圖所示。

    ![顯示 Beta 版面配置範例的圖表。](images/content-view/layout3.png)

-   下圖顯示當專案具有350圖元或更多水準空間時的 Beta 版面配置。

    ![顯示電子郵件 Beta 版面配置範例的螢幕擷取畫面。](images/content-view/betaviewmore.png)

-   下圖顯示當專案的水準空間小於350圖元時的 Beta 版面配置。

    ![顯示 Beta 版面配置範例的圖表，其水準空間小於350圖元。](images/content-view/layout4.png)

-   下圖顯示當專案的水準空間小於350圖元時的 Beta 版面配置：

    ![Beta 版面配置範例](images/content-view/betaviewless.png)

**Gamma 版面配置**

Gamma 配置模式類似于 Alpha，但會使用兩行配置，而不是四個線條的版面配置。 如果您想要查看程式碼片段，但想要在螢幕上容納更多專案，或針對需要較少空間來顯示最重要資訊的檔案類型，則這種版面配置很適合。 Gamma 版面配置具有下列規格：

-   資料列：2
-   屬性：4
-   下圖顯示當專案具有350圖元或更多水準空間時的 gamma 版面配置。

    ![顯示 gamma 版面配置範例的圖表。](images/content-view/layout5.png)

-   下圖顯示當專案具有350圖元或更多水準空間時的 gamma 版面配置。

    ![顯示檢查清單專案之 gamma 版面配置範例的螢幕擷取畫面。](images/content-view/gammaviewmore.png)

-   下圖顯示當專案的水準空間小於350圖元時的 gamma 版面配置。

    ![顯示 gamma 版面配置範例的圖表，其水準空間小於350圖元。](images/content-view/layout6.png)

-   當專案的水準空間小於350圖元時，gamma 配置的範例。

    ![gamma 版面配置範例](images/content-view/gammaviewless.png)

**差異版面配置**

差異配置模式最適合用來顯示許多較短的屬性，例如音樂和圖片。 它具有下列規格：

-   資料列：2
-   屬性：6
-   當專案具有700圖元或更多水準空間時的差異版面配置，如下圖所示。

    ![顯示差異版面配置範例的圖表。](images/content-view/layout7.png)

-   當專案具有700圖元或更多水準空間時的差異版面配置範例。

    ![顯示音樂檔案差異版面配置範例的螢幕擷取畫面。](images/content-view/deltalayoutmore.png)

-   當專案在水準空間的350到700圖元之間時，差異版面配置。

    ![顯示差異版面配置範例的圖表，其水準空間的350和700圖元之間。](images/content-view/layout8.png)

-   當專案在水準空間的350和700圖元之間時，差異版面配置的範例。

    ![差異版面配置範例](images/content-view/deltaviewbetween.png)

-   當專案的水準空間小於350圖元時，則為差異版面配置。

    ![版面配置範例](images/content-view/layout9.png)

-   當專案的水準空間小於350圖元時，差異版面配置的範例。

    ![螢幕擷取畫面，顯示在水準空間小於350圖元之音樂檔案的差異版面配置範例。](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>步驟3：註冊您的檔案類型的自訂屬性和版面配置

當您瞭解搜尋結果模式、瀏覽模式和版面配置模式之後，就可以為您的檔案類型註冊自訂屬性清單。

**註冊檔案類型的自訂屬性清單和配置模式。**

1.  從四種版面配置模式中選擇： Alpha、Beta、Gamma 或 Delta。
2.  請考慮下列格式化規則，這同樣適用于全部四種版面配置模式：
    -   屬性1一律會以較大的字型大小顯示。 大型字型大小通常用於專案名稱，但也可以用於錨點或其他專案屬性。
    -   屬性4適用于 Alpha、Beta 和 Gamma 版面配置模式中的摘錄。 這個屬性會在這些模式中配置更多空間，並以灰色字型色彩顯示，而不像其他屬性一樣黑色，以協助它脫穎而出。
    -   下方的圖元測量是以相對圖元為單位，而大小則包含屬性左邊的圖示/縮圖，以及圖示/縮圖和選取矩形之間的間距。
    -   大部分屬性都有最小的顯示大小。 因此，如果沒有足夠的空間可供特定的視圖大小使用，它們就不會出現。 大小下限通常是100圖元寬。
    -   每個配置模式都會定義每個資料列中的資料列數目和屬性數目。
3.  決定您想要在版面配置中顯示哪些屬性，以及要在每個位置顯示哪個屬性。 當您決定要在版面配置中的每個位置顯示哪一個屬性時，請考慮屬性的一般長度、對使用者的重要性，以及當視窗大小太小而無法包含所有屬性時是否應該卸載。
4.  為您的檔案類型或專案類型，在此範例中的檔案類型或專案 (的 ProgID 登錄機碼底下加入下列索引鍵，以註冊配置模式和屬性清單，) 的 [xyz] 檔案類型。

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  請觀察下列用於註冊屬性的格式化指導方針：

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

     (ContentViewModeForBrowse) 的可能值包括下列各項：： ~ System. ItemNameDisplay;System. Author;LayoutPattern。預留位置;System.string;System. DateModified;~ System. Size

## <a name="remarks"></a>備註

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[種類名稱](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
