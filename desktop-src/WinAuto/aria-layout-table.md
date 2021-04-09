---
title: ARIA 展示表錯誤
description: ARIA 展示表錯誤
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684179"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="b4a86-104">ARIA 展示表錯誤</span><span class="sxs-lookup"><span data-stu-id="b4a86-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="b4a86-105">Text</span><span class="sxs-lookup"><span data-stu-id="b4a86-105">Text</span></span>

<span data-ttu-id="b4a86-106">用於配置的資料表不能有標頭、可存取的名稱或摘要資訊 (**第** 一個、 **摘要**、 **aria-describedby**、 **aria labelledby**、 **aria 標籤**、 **標題**、 **標題** 屬性) 定義。</span><span class="sxs-lookup"><span data-stu-id="b4a86-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="b4a86-107">類型</span><span class="sxs-lookup"><span data-stu-id="b4a86-107">Type</span></span>

<span data-ttu-id="b4a86-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="b4a86-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="b4a86-109">描述</span><span class="sxs-lookup"><span data-stu-id="b4a86-109">Description</span></span>

<span data-ttu-id="b4a86-110">此錯誤適用于將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為 "presentation" 的 HTML 資料表標記，或是具有單一資料格 (1 ×1資料表) 的資料表。</span><span class="sxs-lookup"><span data-stu-id="b4a86-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="b4a86-111">此錯誤表示資料表標示為僅限配置 (有 `role="presentation"`) ，但它也包含協助工具資訊，就像是資料表一樣，這可能會對螢幕閱讀程式使用者造成混淆。</span><span class="sxs-lookup"><span data-stu-id="b4a86-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="b4a86-112">若要解決此錯誤，請判斷資料表是否真的只是版面配置表，如果是的話，請移除可存取的標記：</span><span class="sxs-lookup"><span data-stu-id="b4a86-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="b4a86-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) 元素、 [**aria labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria 標籤**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)或 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b4a86-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="b4a86-114">[**摘要**](https://www.bing.com/search?q=**summary**) 或 [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b4a86-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="b4a86-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) 標記。</span><span class="sxs-lookup"><span data-stu-id="b4a86-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="b4a86-116">範例</span><span class="sxs-lookup"><span data-stu-id="b4a86-116">Example</span></span>

![<span data-ttu-id="b4a86-117">資料表元素的 html，其屬性（例如摘要）會觸發 aria 展示表錯誤，並顯示為使用超時 html 標記</span><span class="sxs-lookup"><span data-stu-id="b4a86-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="b4a86-118">備註</span><span class="sxs-lookup"><span data-stu-id="b4a86-118">Remarks</span></span>

<span data-ttu-id="b4a86-119">如果您判斷資料表確實需要協助工具資訊，請移除 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性，或將它設定為 [presentation] 以外的值。</span><span class="sxs-lookup"><span data-stu-id="b4a86-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




