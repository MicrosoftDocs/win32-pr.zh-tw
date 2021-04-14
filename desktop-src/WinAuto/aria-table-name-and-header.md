---
title: ARIA 資料表錯誤
description: ARIA 資料表錯誤
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383102"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="36228-104">ARIA 資料表錯誤</span><span class="sxs-lookup"><span data-stu-id="36228-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="36228-105">Text</span><span class="sxs-lookup"><span data-stu-id="36228-105">Text</span></span>

<span data-ttu-id="36228-106">資料表包含資料，但沒有透過 **aria 標籤**、 **aria-labelledby**、 **title**、 **caption** 或 **th** 元素所定義的可存取標記。</span><span class="sxs-lookup"><span data-stu-id="36228-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="36228-107">類型</span><span class="sxs-lookup"><span data-stu-id="36228-107">Type</span></span>

<span data-ttu-id="36228-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="36228-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="36228-109">描述</span><span class="sxs-lookup"><span data-stu-id="36228-109">Description</span></span>

<span data-ttu-id="36228-110">此錯誤適用于具有一個以上資料格的 HTML 資料表。</span><span class="sxs-lookup"><span data-stu-id="36228-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="36228-111">此錯誤不會套用至資料表， `role="presentation"` 因為這些會被視為版面配置資料表。</span><span class="sxs-lookup"><span data-stu-id="36228-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="36228-112">此錯誤表示資料表格沒有可存取的名稱或標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="36228-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="36228-113">若要修正這個錯誤，請使用 [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) 標記或 [**aria labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria 標籤**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)或 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性來定義可存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="36228-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="36228-114">如果資料表缺少標頭資訊，請使用 [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) 標記來標示標頭儲存格。</span><span class="sxs-lookup"><span data-stu-id="36228-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="36228-115">範例</span><span class="sxs-lookup"><span data-stu-id="36228-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




