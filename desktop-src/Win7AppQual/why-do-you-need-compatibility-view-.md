---
description: 為什麼需要相容性檢視？
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: 為什麼需要相容性檢視？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9991e9dc0c2edcd66ae6655c094f17b240be985a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113376"
---
# <a name="why-do-you-need-compatibility-view"></a><span data-ttu-id="8a05d-103">為什麼需要相容性檢視？</span><span class="sxs-lookup"><span data-stu-id="8a05d-103">Why Do You Need Compatibility View?</span></span>

<span data-ttu-id="8a05d-104">相容性檢視功能會遵循一組規則，以正確顯示內容，而不需要任何使用者 (或 IT 系統管理員) 動作（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="8a05d-104">The Compatibility View feature follows a set of rules to display content correctly, without any user (or IT administrator) action needed whenever possible.</span></span> <span data-ttu-id="8a05d-105">相容性檢視可讓開發人員指示瀏覽器要使用的轉譯引擎，並讓使用者覆寫瀏覽器的選擇和切換模式。</span><span class="sxs-lookup"><span data-stu-id="8a05d-105">Compatibility View enables developers to instruct the browser which rendering engine to use and enables users to override the browser’s choice and switch modes.</span></span> <span data-ttu-id="8a05d-106">如果開發人員和 IT 專業人員未指定要使用哪種轉譯模式，則使用者會在網址列的右邊看到「中斷的頁面」圖示，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8a05d-106">If the developer and IT professional do not specify which rendering mode to use, user sees the "broken page" icon at the right end of the address bar, as the following illustration shows.</span></span>

![網址列旁的中斷頁面圖示圖例](images/iecompatview.png)

<span data-ttu-id="8a05d-108">如果使用者按一下此圖示，Windows Internet Explorer 8 會切換轉譯模式，並立即重載頁面。</span><span class="sxs-lookup"><span data-stu-id="8a05d-108">If a user clicks the icon, Windows Internet Explorer 8 switches rendering modes, and the page reloads instantly.</span></span>

<span data-ttu-id="8a05d-109">使用者不一定會看到這個圖示。</span><span class="sxs-lookup"><span data-stu-id="8a05d-109">Users do not always see this icon.</span></span> <span data-ttu-id="8a05d-110">它是次要解決方案，而不是主要的應用程式相容性機制。</span><span class="sxs-lookup"><span data-stu-id="8a05d-110">It is a secondary solution instead of the primary application compatibility mechanism.</span></span> <span data-ttu-id="8a05d-111">只有當相容性檢視的變更有意義時（例如當使用者流覽標準模式頁面時），Windows Internet Explorer 才會顯示此圖示。</span><span class="sxs-lookup"><span data-stu-id="8a05d-111">Windows Internet Explorer displays this icon only when a change into Compatibility View makes sense, such as when a user views standards mode pages.</span></span> <span data-ttu-id="8a05d-112">在所有其他情況下，例如當使用者查看 [其他] 模式頁面或 [view 近端內部網路] 區域網站時，不會出現此圖示。</span><span class="sxs-lookup"><span data-stu-id="8a05d-112">In all other cases, such as when a user views quirks mode pages or views Intranet Zone sites, the icon does not appear.</span></span> <span data-ttu-id="8a05d-113">如需相容性檢視的詳細資訊，以及出現圖示時，請參閱 [相容性檢視簡介](/archive/blogs/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8a05d-113">For more information about Compatibility View and when the icon appears, see [Introducing Compatibility View](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a05d-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a05d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a05d-115">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="8a05d-115">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
