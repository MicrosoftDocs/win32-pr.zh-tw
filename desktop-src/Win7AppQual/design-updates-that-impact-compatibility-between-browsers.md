---
description: 設計影響瀏覽器相容性的更新
ms.assetid: F2C13FEC-5537-4B0D-BFDB-E17A42A289CB
title: 設計影響瀏覽器相容性的更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a306a64cb03bce8b466f6367339302522109619a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088476"
---
# <a name="design-updates-that-impact-compatibility-between-browsers"></a><span data-ttu-id="1bc2b-103">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="1bc2b-103">Design Updates that Impact Compatibility between Browsers</span></span>

<span data-ttu-id="1bc2b-104">此區段和下表顯示 (的四個主要區域，而不是依優先順序) 的出現順序或排名。</span><span class="sxs-lookup"><span data-stu-id="1bc2b-104">This section and the following table show the four major areas of compatibility (not in order of incidence or ranking of priority).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1bc2b-105">從 Internet Explorer 6 到 Internet Explorer 7 的變更</span><span class="sxs-lookup"><span data-stu-id="1bc2b-105">Changes from Internet Explorer 6 to Internet Explorer 7</span></span></th>
<th><span data-ttu-id="1bc2b-106">從 Internet Explorer 7 到 Internet Explorer 8 的變更</span><span class="sxs-lookup"><span data-stu-id="1bc2b-106">Changes from Internet Explorer 7 to Internet Explorer 8</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1bc2b-107"><a href="versioning.md">版本控制</a></span><span class="sxs-lookup"><span data-stu-id="1bc2b-107"><a href="versioning.md">Versioning</a></span></span></td>
<td><ul>
<li><span data-ttu-id="1bc2b-108">版本向量</span><span class="sxs-lookup"><span data-stu-id="1bc2b-108">Version Vectors</span></span></li>
<li><span data-ttu-id="1bc2b-109">使用者代理程式字串</span><span class="sxs-lookup"><span data-stu-id="1bc2b-109">User Agent String</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1bc2b-110">版本向量</span><span class="sxs-lookup"><span data-stu-id="1bc2b-110">Version Vectors</span></span></li>
<li><span data-ttu-id="1bc2b-111">使用者代理程式字串</span><span class="sxs-lookup"><span data-stu-id="1bc2b-111">User Agent String</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bc2b-112"><a href="standards.md">標準</a></span><span class="sxs-lookup"><span data-stu-id="1bc2b-112"><a href="standards.md">Standards</a></span></span></td>
<td><ul>
<li><span data-ttu-id="1bc2b-113">HTML 4.01 改進</span><span class="sxs-lookup"><span data-stu-id="1bc2b-113">HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="1bc2b-114">CSS 2.1 改進</span><span class="sxs-lookup"><span data-stu-id="1bc2b-114">CSS 2.1 improvements</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1bc2b-115">其他 HTML 4.01 改進</span><span class="sxs-lookup"><span data-stu-id="1bc2b-115">Additional HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="1bc2b-116">完整的 CSS 2.1 合規性</span><span class="sxs-lookup"><span data-stu-id="1bc2b-116">Full CSS 2.1 compliance</span></span></li>
<li><span data-ttu-id="1bc2b-117">一些 HTML 5.0 支援</span><span class="sxs-lookup"><span data-stu-id="1bc2b-117">Some HTML 5.0 support</span></span></li>
<li><span data-ttu-id="1bc2b-118">ECMAScript 第3版支援和某些 ECMAScript 5 版本支援 (包括原生 JSON) </span><span class="sxs-lookup"><span data-stu-id="1bc2b-118">ECMAScript 3rd edition support and some ECMAScript 5th edition support (including native JSON)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bc2b-119"><a href="security.md">安全性</a></span><span class="sxs-lookup"><span data-stu-id="1bc2b-119"><a href="security.md">Security</a></span></span></td>
<td><ul>
<li><span data-ttu-id="1bc2b-120">HTTPS 改進</span><span class="sxs-lookup"><span data-stu-id="1bc2b-120">HTTPS improvements</span></span></li>
<li><span data-ttu-id="1bc2b-121">更安全的腳本</span><span class="sxs-lookup"><span data-stu-id="1bc2b-121">More secure scripting</span></span></li>
<li><span data-ttu-id="1bc2b-122">受保護模式 (Windows Vista 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="1bc2b-122">Protected Mode (Windows Vista and later versions)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="1bc2b-123">更妥善防範惡意軟體</span><span class="sxs-lookup"><span data-stu-id="1bc2b-123">Better protection from malware</span></span></li>
<li><span data-ttu-id="1bc2b-124">預設的 DEP/NX & XSS 篩選器</span><span class="sxs-lookup"><span data-stu-id="1bc2b-124">DEP/NX & XSS filter on by default</span></span></li>
<li><span data-ttu-id="1bc2b-125">HTTP/HTTPS 混合模式</span><span class="sxs-lookup"><span data-stu-id="1bc2b-125">HTTP/HTTPS mixed mode</span></span></li>
<li><span data-ttu-id="1bc2b-126">AJAX 更安全</span><span class="sxs-lookup"><span data-stu-id="1bc2b-126">AJAX more secure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bc2b-127"><a href="architecture.md">架構</a></span><span class="sxs-lookup"><span data-stu-id="1bc2b-127"><a href="architecture.md">Architecture</a></span></span></td>

<td><ul>
<li><span data-ttu-id="1bc2b-128">鬆散結合的 Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1bc2b-128">Loosely coupled Internet Explorer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1bc2b-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bc2b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bc2b-130">在遷移至 Internet Explorer 8 時解決應用程式相容性問題</span><span class="sxs-lookup"><span data-stu-id="1bc2b-130">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



