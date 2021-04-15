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
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462921"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="cb51c-106">類別和屬性顯示名稱</span><span class="sxs-lookup"><span data-stu-id="cb51c-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="cb51c-107">物件類別的顯示規範包含下列屬性，這些屬性可以用來指定用於該類別物件之 UI 中的當地語系化顯示名稱：</span><span class="sxs-lookup"><span data-stu-id="cb51c-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="cb51c-108">**ClassDisplayName** 屬性是指定類別顯示名稱的單一值 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="cb51c-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="cb51c-109">**AttributeDisplayNames** 屬性是多重值屬性，可指定要在 UI 中用於物件類別之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb51c-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="cb51c-110">**AttributeDisplayNames** 值為 Unicode 字串;每個元素都包含逗點分隔的名稱組：</span><span class="sxs-lookup"><span data-stu-id="cb51c-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="cb51c-111">在此範例中，「 &lt; 屬性名稱」 &gt; 是屬性的 **lDAPDisplayName** ，而「 &lt; 顯示文字」 &gt; 是在使用者介面中顯示為該屬性名稱的文字。</span><span class="sxs-lookup"><span data-stu-id="cb51c-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="cb51c-112">類別和屬性顯示名稱的指導方針</span><span class="sxs-lookup"><span data-stu-id="cb51c-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="cb51c-113">因為許多廠商可能會以新的屬性來擴充類別，或建立全新的類別，所以類別和屬性顯示名稱很重要，且不會導致衝突。</span><span class="sxs-lookup"><span data-stu-id="cb51c-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="cb51c-114">每個廠商都應該使用以廠商名稱為基礎的唯一易記識別碼，在類別顯示名稱前面加上前置詞。</span><span class="sxs-lookup"><span data-stu-id="cb51c-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="cb51c-115">例如，假設虛構公司 Fabrikam Inc. 建立了衍生自 "contact" 類別的新類別，他們可以有唯一的類別顯示名稱 "Fabrikam Contact"。</span><span class="sxs-lookup"><span data-stu-id="cb51c-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="cb51c-116">如果廠商以新的屬性來擴充現有的類別，則應該再次以唯一的方式識別屬性顯示名稱，讓其他屬性顯示名稱不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="cb51c-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="cb51c-117">同樣地，在屬性顯示名稱前面加上以廠商名稱為基礎的唯一易記識別碼是不錯的作法。</span><span class="sxs-lookup"><span data-stu-id="cb51c-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="cb51c-118">例如，假設 Fabrikam 公司以新的 HR 屬性擴充使用者類別，則可以將屬性唯一顯示為「Fabrikam HR 資訊」。</span><span class="sxs-lookup"><span data-stu-id="cb51c-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="cb51c-119">此外，從當地語系化的觀點來看，每個廠商都應該將類別和屬性顯示名稱當地語系化為 Windows 2000 所支援的每種語言。</span><span class="sxs-lookup"><span data-stu-id="cb51c-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="cb51c-120">將值加入至 attributeDisplayNames 屬性</span><span class="sxs-lookup"><span data-stu-id="cb51c-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="cb51c-121">**若要將名稱對應值加入至 **attributeDisplayNames** 屬性**</span><span class="sxs-lookup"><span data-stu-id="cb51c-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="cb51c-122">判斷屬性的名稱對應值是否存在。</span><span class="sxs-lookup"><span data-stu-id="cb51c-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="cb51c-123">如果要取代名稱對應值，請先使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法來刪除現有的值，並將 *lnControlCode* 參數設定為 **ADS \_ PROPERTY \_ DELETE** ，並將 *vProp* 參數設定為要移除的值。</span><span class="sxs-lookup"><span data-stu-id="cb51c-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="cb51c-124">請勿使用 *lnControlCode* 的 **ads \_ 屬性 \_ CLEAR** 或 **ads \_ 屬性 \_ 更新**。</span><span class="sxs-lookup"><span data-stu-id="cb51c-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="cb51c-125">建立表示屬性顯示名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="cb51c-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="cb51c-126">如需範例，請參閱上面的格式。</span><span class="sxs-lookup"><span data-stu-id="cb51c-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="cb51c-127">使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法，並將 *lnControlCode* 參數設定為 **ADS \_ 屬性 \_ 附加** ，以加入新的值。</span><span class="sxs-lookup"><span data-stu-id="cb51c-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="cb51c-128">呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可目錄的變更。</span><span class="sxs-lookup"><span data-stu-id="cb51c-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="cb51c-129">如需命名新類別和屬性的詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="cb51c-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 