---
description: 版本向量會處理 HTML 網頁中的條件式批註。 也就是說，版本向量可讓您根據瀏覽器版本建立標記。
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: 版本向量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321195"
---
# <a name="version-vectors"></a><span data-ttu-id="3f890-104">版本向量</span><span class="sxs-lookup"><span data-stu-id="3f890-104">Version Vectors</span></span>

<span data-ttu-id="3f890-105">*版本向量* 會處理 HTML 網頁中的條件式批註。</span><span class="sxs-lookup"><span data-stu-id="3f890-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="3f890-106">也就是說，版本向量可讓您根據瀏覽器版本建立標記。</span><span class="sxs-lookup"><span data-stu-id="3f890-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="3f890-107">請考慮下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="3f890-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="3f890-108">在此情況下，如果 Windows Internet Explorer 瀏覽器版本至少為5.5，則網頁上會顯示對應的段落。</span><span class="sxs-lookup"><span data-stu-id="3f890-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="3f890-109">雖然此範例中的第一個條件說明條件式批註的函式，但這些批註通常不會用來顯示第一個條件之類的標記。</span><span class="sxs-lookup"><span data-stu-id="3f890-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="3f890-110">相反地，上述範例中的其餘條件式批註更為常見。</span><span class="sxs-lookup"><span data-stu-id="3f890-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="3f890-111">在這些其餘的批註中，條件式批註會針對不同版本的瀏覽器使用不同的樣式表單。</span><span class="sxs-lookup"><span data-stu-id="3f890-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="3f890-112">上述程式碼範例也會檢查 Microsoft Internet Explorer 6 和 Windows Internet Explorer 7 是否相等。</span><span class="sxs-lookup"><span data-stu-id="3f890-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="3f890-113">但是針對 Windows Internet Explorer 8，此範例會使用 gte 運算子 (大於或等於) 。</span><span class="sxs-lookup"><span data-stu-id="3f890-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="3f890-114">這個運算子可協助您在未來進行此範例，以便在發行新版的瀏覽器時，使用樣式表單最符合標準的版本 (而不是使用錯誤的樣式表單或沒有樣式表單) 。</span><span class="sxs-lookup"><span data-stu-id="3f890-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="3f890-115">現有的應用程式通常不會考慮 Internet Explorer 過去 7 (的版本，或網站為) 建立的最新版本 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="3f890-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="3f890-116">如需版本向量的詳細資訊，請參閱 MSDN Library 中的 [版本向量](/previous-versions/cc817577(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="3f890-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f890-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f890-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f890-118">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="3f890-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



