---
title: 類別和屬性顯示名稱
description: 本主題包含類別和屬性顯示名稱的相關資訊與指導方針。
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- 顯示規範： AD、類別和屬性顯示名稱
- 類別顯示名稱廣告
- 屬性顯示名稱廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213132acfa6463b1c1e8a7615f5d7f488e53edfcdf9b75f8df5759fcd0e4d398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022589"
---
# <a name="class-and-attribute-display-names"></a>類別和屬性顯示名稱

物件類別的顯示規範包含下列屬性，這些屬性可以用來指定用於該類別物件之 UI 中的當地語系化顯示名稱：

-   **ClassDisplayName** 屬性是指定類別顯示名稱的單一值 Unicode 字串。
-   **AttributeDisplayNames** 屬性是多重值屬性，可指定要在 UI 中用於物件類別之屬性的名稱。

**AttributeDisplayNames** 值為 Unicode 字串;每個元素都包含逗點分隔的名稱組：


```C++
<attribute name>,<display text>
```



在此範例中，「 &lt; 屬性名稱」 &gt; 是屬性的 **lDAPDisplayName** ，而「 &lt; 顯示文字」 &gt; 是在使用者介面中顯示為該屬性名稱的文字。

## <a name="guidelines-for-class-and-attribute-display-names"></a>類別和屬性顯示名稱的指導方針

因為許多廠商可能會以新的屬性來擴充類別，或建立全新的類別，所以類別和屬性顯示名稱很重要，且不會導致衝突。

每個廠商都應該使用以廠商名稱為基礎的唯一易記識別碼，在類別顯示名稱前面加上前置詞。 例如，假設虛構公司 Fabrikam Inc. 建立了衍生自 "contact" 類別的新類別，他們可以有唯一的類別顯示名稱 "Fabrikam Contact"。

如果廠商以新的屬性來擴充現有的類別，則應該再次以唯一的方式識別屬性顯示名稱，讓其他屬性顯示名稱不會發生衝突。 同樣地，在屬性顯示名稱前面加上以廠商名稱為基礎的唯一易記識別碼是不錯的作法。 例如，假設 Fabrikam 公司以新的 HR 屬性擴充使用者類別，則可以將屬性唯一顯示為「Fabrikam HR 資訊」。

此外，從當地語系化的觀點來看，每個廠商都應該將類別和屬性顯示名稱當地語系化為 Windows 2000 所支援的每種語言。

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>將值加入至 attributeDisplayNames 屬性

**若要將名稱對應值加入至 **attributeDisplayNames** 屬性**

1.  判斷屬性的名稱對應值是否存在。 如果要取代名稱對應值，請先使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法來刪除現有的值，並將 *lnControlCode* 參數設定為 **ADS \_ PROPERTY \_ DELETE** ，並將 *vProp* 參數設定為要移除的值。 請勿使用 *lnControlCode* 的 **ads \_ 屬性 \_ CLEAR** 或 **ads \_ 屬性 \_ 更新**。
2.  建立表示屬性顯示名稱的字串。 如需範例，請參閱上面的格式。
3.  使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法，並將 *lnControlCode* 參數設定為 **ADS \_ 屬性 \_ 附加** ，以加入新的值。
4.  呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可目錄的變更。

如需命名新類別和屬性的詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。

 

 