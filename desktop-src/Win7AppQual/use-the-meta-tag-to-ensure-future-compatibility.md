---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: 使用中繼標記以確保未來的相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981706"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="6b4b1-103">使用中繼標記以確保未來的相容性</span><span class="sxs-lookup"><span data-stu-id="6b4b1-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="6b4b1-104">Windows Internet Explorer 8 可讓您控制檔相容性模式，因此您可以指示瀏覽器以與舊版瀏覽器版本相同的方式轉譯網頁。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="6b4b1-105">您也可以選擇何時更新網頁，但仍可繼續使用且正常運作。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="6b4b1-106">設定中繼元素</span><span class="sxs-lookup"><span data-stu-id="6b4b1-106">Setting the Meta Element</span></span>

<span data-ttu-id="6b4b1-107">**中繼** 元素包含 **內容** 屬性，可讓您指定在網頁中呈現內容的模式，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="6b4b1-108">值</span><span class="sxs-lookup"><span data-stu-id="6b4b1-108">Value</span></span> | <span data-ttu-id="6b4b1-109">轉譯模式</span><span class="sxs-lookup"><span data-stu-id="6b4b1-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="6b4b1-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="6b4b1-110">IE=9</span></span>  | <span data-ttu-id="6b4b1-111">使用 Windows Internet Explorer 9 標準轉譯模式</span><span class="sxs-lookup"><span data-stu-id="6b4b1-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="6b4b1-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="6b4b1-112">IE=8</span></span>  | <span data-ttu-id="6b4b1-113">使用 Internet Explorer 8 標準轉譯模式</span><span class="sxs-lookup"><span data-stu-id="6b4b1-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="6b4b1-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="6b4b1-114">IE=7</span></span>  | <span data-ttu-id="6b4b1-115">使用 Windows Internet Explorer 7 標準轉譯模式</span><span class="sxs-lookup"><span data-stu-id="6b4b1-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="6b4b1-116">IE = 5</span><span class="sxs-lookup"><span data-stu-id="6b4b1-116">IE=5</span></span>  | <span data-ttu-id="6b4b1-117">使用 Microsoft Internet Explorer 5 標準轉譯模式</span><span class="sxs-lookup"><span data-stu-id="6b4b1-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="6b4b1-118">如需相容性和 X-UA 相容標頭的詳細資訊，請參閱 MSDN Library 中的 [定義檔相容性](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="6b4b1-119">下列程式碼範例將示範如何強制網頁在 Internet Explorer 8 模式中呈現。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="6b4b1-120">使用 HTTP 標頭</span><span class="sxs-lookup"><span data-stu-id="6b4b1-120">Using an HTTP Header</span></span>

<span data-ttu-id="6b4b1-121">許多網站都包含數千 (或數萬個個別網頁的) ，因此在每個檔上設定 **中繼** 元素是不切實際的。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="6b4b1-122">如果您想要設定所有頁面的 **中繼** 元素或資料夾所選取的頁面集合，您可以改為調整伺服器設定，並在 [HTTP 標頭](/previous-versions/cc817572(v=msdn.10))中新增 X-UA 相容的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="6b4b1-123">針對相同伺服器上的頁面需要不同 **中繼** 元素值的網站，有數個工具會自動為您產生並插入適當的 **中繼** 元素。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="6b4b1-124">例如，來自 Aggiorno 的 [ArtinSoft Web 工具](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) 公用程式會插入和移除 Internet Explorer 8 相容性標記功能，並可協助您的網站符合特定的相容性標準。</span><span class="sxs-lookup"><span data-stu-id="6b4b1-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b4b1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b4b1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b4b1-126">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="6b4b1-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
