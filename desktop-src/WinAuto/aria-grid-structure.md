---
title: ARIA 方格結構錯誤
description: ARIA 方格結構錯誤
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684181"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="53f42-104">ARIA 方格結構錯誤</span><span class="sxs-lookup"><span data-stu-id="53f42-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="53f42-105">Text</span><span class="sxs-lookup"><span data-stu-id="53f42-105">Text</span></span>

<span data-ttu-id="53f42-106">具有 **方格** 角色的元素沒有對應的方格結構或可存取的標記。</span><span class="sxs-lookup"><span data-stu-id="53f42-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="53f42-107">類型</span><span class="sxs-lookup"><span data-stu-id="53f42-107">Type</span></span>

<span data-ttu-id="53f42-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="53f42-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="53f42-109">描述</span><span class="sxs-lookup"><span data-stu-id="53f42-109">Description</span></span>

<span data-ttu-id="53f42-110">此錯誤適用于 **role** 屬性設為 "grid" 的自訂元素。</span><span class="sxs-lookup"><span data-stu-id="53f42-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="53f42-111">它並不適用于具有「方格」隱含 **角色** 的 HTML 資料表標記。</span><span class="sxs-lookup"><span data-stu-id="53f42-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="53f42-112">將其 **role** 屬性設定為 "grid" 的元素，必須具有由 Web 協助工具輔助的豐富網際網路應用程式所定義的結構 (WAI-ARIA) 方格角色，包括方格的可存取名稱和其標頭子項目。</span><span class="sxs-lookup"><span data-stu-id="53f42-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="53f42-113">若要修正這個錯誤，請檢查您的執行方式，以確定它符合 WAI-ARIA 規格。</span><span class="sxs-lookup"><span data-stu-id="53f42-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="53f42-114">具體而言，請確定結構符合下列規則。</span><span class="sxs-lookup"><span data-stu-id="53f42-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="53f42-115">**方格** 包含資料列 **或資料\*\*\*\*列** 群組元素。</span><span class="sxs-lookup"><span data-stu-id="53f42-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="53f42-116">資料列 **群組包含資料\*\*\*\*列** 元素。</span><span class="sxs-lookup"><span data-stu-id="53f42-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="53f42-117">**row** 元素包含 **columnheader** 或 **gridcell** 或 **rowheader** 元素。</span><span class="sxs-lookup"><span data-stu-id="53f42-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="53f42-118">您應使用下列其中一個屬性，為 **grid**、 **columnheader**、 **gridcell** 和 **rowheader** 元素定義可存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="53f42-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="53f42-119">[**labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，用於參考包含文字的元素。</span><span class="sxs-lookup"><span data-stu-id="53f42-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="53f42-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，可直接設定可存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="53f42-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="53f42-121">用來建立工具提示的 [**標題**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title)，該工具提示同時作為名稱使用。</span><span class="sxs-lookup"><span data-stu-id="53f42-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 




