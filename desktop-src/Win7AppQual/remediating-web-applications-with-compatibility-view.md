---
description: 使用相容性檢視修正 Web 應用程式中的相容性問題
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: 使用相容性檢視修正 Web 應用程式中的相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116356"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="3ffb5-103">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="3ffb5-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="3ffb5-104">本節說明基本的風險降低步驟，以及如何在您立即解決任何問題時規劃未來的應用程式相容性。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="3ffb5-105">Windows Internet Explorer 會在可行時支援舊版 Internet Explorer 模型，讓您開發的網站在較新版本的 Internet Explorer 中繼續以預期的方式運作。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="3ffb5-106">從 Windows Internet Explorer 8 開始，您可以選擇依頁面逐一選取轉譯模式，以支援舊版行為。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="3ffb5-107">Internet Explorer 8 包含下列轉譯模式，您可以使用與 X-UA 相容的標頭來設定這些模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="3ffb5-108">內容值</span><span class="sxs-lookup"><span data-stu-id="3ffb5-108">Content value</span></span> | <span data-ttu-id="3ffb5-109">Description</span><span class="sxs-lookup"><span data-stu-id="3ffb5-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffb5-110">IE = 5</span><span class="sxs-lookup"><span data-stu-id="3ffb5-110">IE=5</span></span>          | <span data-ttu-id="3ffb5-111">使用 [不相容] 模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="3ffb5-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="3ffb5-112">IE=7</span></span>          | <span data-ttu-id="3ffb5-113">一律使用 Windows Internet Explorer 7 模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="3ffb5-114">IE = EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="3ffb5-114">IE=EmulateIE7</span></span> | <span data-ttu-id="3ffb5-115">除非網站具有不相容的 DOCTYPE，否則會顯示 Internet Explorer 7 模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="3ffb5-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="3ffb5-116">IE=8</span></span>          | <span data-ttu-id="3ffb5-117">一律使用 Internet Explorer 8 模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="3ffb5-118">IE = EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="3ffb5-118">IE=EmulateIE8</span></span> | <span data-ttu-id="3ffb5-119">覆寫用戶端電腦上的相容性檢視，並使用 Internet Explorer 8 模式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="3ffb5-120">IE = 邊緣</span><span class="sxs-lookup"><span data-stu-id="3ffb5-120">IE=Edge</span></span>       | <span data-ttu-id="3ffb5-121">以最新模式顯示。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-121">Display in the latest mode.</span></span> <span data-ttu-id="3ffb5-122">在 Internet Explorer 8 中，此值相當於 IE = 8。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="3ffb5-123">下列主題描述如何使用相容性檢視來更新 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="3ffb5-124">主題</span><span class="sxs-lookup"><span data-stu-id="3ffb5-124">Topic</span></span>                                                                                                  | <span data-ttu-id="3ffb5-125">描述</span><span class="sxs-lookup"><span data-stu-id="3ffb5-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="3ffb5-126">什麼是相容性檢視</span><span class="sxs-lookup"><span data-stu-id="3ffb5-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="3ffb5-127">描述相容性檢視。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="3ffb5-128">為什麼需要相容性檢視？</span><span class="sxs-lookup"><span data-stu-id="3ffb5-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="3ffb5-129">描述您應該使用相容性檢視的原因。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="3ffb5-130">使用中繼標記以確保未來的相容性</span><span class="sxs-lookup"><span data-stu-id="3ffb5-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="3ffb5-131">描述如何使用 **中繼** 元素以確保未來的相容性。</span><span class="sxs-lookup"><span data-stu-id="3ffb5-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



