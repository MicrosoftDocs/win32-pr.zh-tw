---
title: " (的 VML) 附錄"
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- 網路研討會，命名空間
- 網路研討會，行為樣式
- 設計網頁、命名空間
- 設計網頁、行為樣式
- Vector Markup Language (VML) 、命名空間
- VML (Vector Markup Language) 、命名空間
- 向量圖形，命名空間
- Vector Markup Language (VML) 、行為樣式
- VML (Vector Markup Language) 、行為樣式
- 向量圖形，行為樣式
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383681"
---
# <a name="appendix-vml"></a><span data-ttu-id="65d38-114"> (的 VML) 附錄</span><span class="sxs-lookup"><span data-stu-id="65d38-114">Appendix (VML)</span></span>

<span data-ttu-id="65d38-115">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="65d38-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="65d38-116">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="65d38-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="65d38-117">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="65d38-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="65d38-118">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="65d38-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="65d38-119">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="65d38-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="65d38-120">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="65d38-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="65d38-121">若要讓瀏覽器知道如何將資料交給 VML 特定的處理器，您需要輸入一些資訊，例如命名空間和行為樣式。</span><span class="sxs-lookup"><span data-stu-id="65d38-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="65d38-122">然後，您可以使用 VML 來輸入區域中的圖形 `<BODY>` 。</span><span class="sxs-lookup"><span data-stu-id="65d38-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="65d38-123">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="65d38-123">In this topic:</span></span>

-   [<span data-ttu-id="65d38-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="65d38-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="65d38-125">行為樣式</span><span class="sxs-lookup"><span data-stu-id="65d38-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="65d38-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="65d38-126">Namespaces</span></span>

<span data-ttu-id="65d38-127">XML 機制指出元素的命名空間。</span><span class="sxs-lookup"><span data-stu-id="65d38-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="65d38-128">如果您從 HTML 中的剖析切換到 XML 中的剖析，此機制會指出 HTML 內的參數。</span><span class="sxs-lookup"><span data-stu-id="65d38-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="65d38-129">要求 vender 您的 VML 處理器需要 XML 命名空間所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="65d38-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="65d38-130">如果您使用 Microsoft Internet Explorer 轉譯 VML，請一律在標記中輸入下列程式 `<HTML>` 程式碼：</span><span class="sxs-lookup"><span data-stu-id="65d38-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="65d38-131">當剖析具有前置詞的 XML 標記 `v:` ，並將產生的資料交給 vml 處理器時，此資訊會告訴 Internet Explorer 切換至命名空間 "urn：架構-microsoft-com： vml"。</span><span class="sxs-lookup"><span data-stu-id="65d38-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="65d38-132">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="65d38-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="65d38-133">行為樣式</span><span class="sxs-lookup"><span data-stu-id="65d38-133">Behavior Styles</span></span>

<span data-ttu-id="65d38-134">在 Microsoft Internet Explorer 中，會將 VML 定義為預設行為。</span><span class="sxs-lookup"><span data-stu-id="65d38-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="65d38-135">若要轉譯 VML，請一律在區域中輸入下列幾行 `<HEAD>` ：</span><span class="sxs-lookup"><span data-stu-id="65d38-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="65d38-136">在 Internet Explorer 中，會透過 VGX.DLL 來執行 VML。</span><span class="sxs-lookup"><span data-stu-id="65d38-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="65d38-137">如果您的瀏覽器初始安裝未包含 VML 行為，您可能需要將它新增為選項。</span><span class="sxs-lookup"><span data-stu-id="65d38-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="65d38-138">您不需要新增 `<object>` 標記。</span><span class="sxs-lookup"><span data-stu-id="65d38-138">You do not need to add an `<object>` tag.</span></span>

 

 
