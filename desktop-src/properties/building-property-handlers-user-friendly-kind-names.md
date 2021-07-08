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
# <a name="using-kind-names"></a><span data-ttu-id="c5d5f-103">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="c5d5f-103">Using Kind Names</span></span>

<span data-ttu-id="c5d5f-104">屬性系統包含名為的屬性 `System.Kind` ，它會根據副檔名將專案分割成類型，以及使用者可以輕鬆地識別。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="c5d5f-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="c5d5f-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c5d5f-106">關於 System.object 屬性</span><span class="sxs-lookup"><span data-stu-id="c5d5f-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="c5d5f-107">種類值階層和註冊</span><span class="sxs-lookup"><span data-stu-id="c5d5f-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="c5d5f-108">其他資源</span><span class="sxs-lookup"><span data-stu-id="c5d5f-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c5d5f-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5d5f-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="c5d5f-110">關於 System.object 屬性</span><span class="sxs-lookup"><span data-stu-id="c5d5f-110">About the System.Kind Property</span></span>

<span data-ttu-id="c5d5f-111">種類是在 Windows Vista 中引進，以表達更容易使用的檔案類型概念。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="c5d5f-112">`System.Kind`屬性會將專案分割成類型，並提供終端使用者可以識別的種類名稱，例如檔、音樂、圖片等等。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="c5d5f-113">因此，種類名稱就稱為「使用者易記」。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="c5d5f-114">因為 `System.Kind` 相同檔案類型的專案會將屬性設定為相同的值，並將具有類似特性的專案與通用屬性產生關聯，所以系統和使用者可以針對整個群組進行動作。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="c5d5f-115">例如， `System.Kind` 屬性可用來限制搜尋特定種類的專案、顯示內容視圖中專案的最相關屬性，或將類似的專案群組在一起。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="c5d5f-116">因為 Kind 是多重值字串屬性，所以您可以有 `audio;video` 或種類的 `link;document` 值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="c5d5f-117">`System.Kind`值是字串值的排序清單。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="c5d5f-118">在某些情況下，該清單中可能只有一個元素。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="c5d5f-119">在其他情況下，專案可以屬於一個以上的類型。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="c5d5f-120">如需屬於一種以上類型的專案範例，請參閱本主題中的登錄機碼範例。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="c5d5f-121">字串值來自一組預先定義的已知值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="c5d5f-122">使用不區分大小寫和不區分地區設定的字串比較函式來比較值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="c5d5f-123">這些字串並不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-123">These strings are not localized.</span></span>

<span data-ttu-id="c5d5f-124">某些種類的名稱已與屬性和配置模式相關聯。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="c5d5f-125">例如，與相關聯的專案 `Kind.Picture` 以及與相關聯的專案， `Kind.Document` 即使它們都在相同的視圖中，也會顯示不同的屬性，因為已與這兩種類型的名稱相關聯的屬性和配置模式。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="c5d5f-126">每個專案種類都可以與四種獨特的版面配置模式之一建立關聯，以定義每個專案和其配置所顯示的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="c5d5f-127">如需詳細資訊，請參閱以 [檔案類型或種類關聯為基礎的內容視圖](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="c5d5f-128">種類值階層和註冊</span><span class="sxs-lookup"><span data-stu-id="c5d5f-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="c5d5f-129">`Kind`值必須代表下列清單中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-129">A `Kind` value must represent one of the values in the following list.</span></span>

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

<span data-ttu-id="c5d5f-130">屬性處理常式可以 `System.Kind` 透過登錄以靜態方式宣告其屬性，也可以透過其程式碼以動態方式提供值，就像使用標準屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="c5d5f-131">若要以靜態 `Kind` 方式定義屬性，會在 **KindMap** 登錄機碼底下加入 **REG \_ SZ** 值專案，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

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

<span data-ttu-id="c5d5f-132">請注意， `Kind` 可以是單一值或分號分隔字串中的多個值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="c5d5f-133">提供多個值時， `Kind` 會先列出最特定的值，並指定下列最小的值。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="c5d5f-134">在此範例中，會先命名 Contact，因為它的階層比通訊更明確。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="c5d5f-135">假設為值 **專案** ，不應該提供明確。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5d5f-136">其他資源</span><span class="sxs-lookup"><span data-stu-id="c5d5f-136">Additional Resources</span></span>

-   <span data-ttu-id="c5d5f-137">如需屬性的參考檔， [請參閱](./props-system-kind.md) [KindText](./props-system-kindtext.md)。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="c5d5f-138">如需建立新的或使用現有檔案類型的詳細資訊，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c5d5f-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5d5f-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5d5f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d5f-140">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d5f-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="c5d5f-141">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="c5d5f-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="c5d5f-142">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d5f-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="c5d5f-143">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d5f-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="c5d5f-144">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="c5d5f-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
