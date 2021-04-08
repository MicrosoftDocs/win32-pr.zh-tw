---
description: .
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: 什麼是相容性檢視？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac72fc5afa0e2946a4f904cbcea3c7b0af723c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695831"
---
# <a name="what-is-compatibility-view"></a><span data-ttu-id="2fc81-103">什麼是相容性檢視？</span><span class="sxs-lookup"><span data-stu-id="2fc81-103">What Is Compatibility View?</span></span>

<span data-ttu-id="2fc81-104">*相容性檢視* 是 windows Internet Explorer 8 的一項功能，可讓瀏覽器轉譯網頁的方式幾乎與 Windows Internet Explorer 7 轉譯網頁的方式相同。</span><span class="sxs-lookup"><span data-stu-id="2fc81-104">*Compatibility View* is a feature of Windows Internet Explorer 8 that enables the browser to render a webpage nearly identically to the way that Windows Internet Explorer 7 would render it.</span></span>

<span data-ttu-id="2fc81-105">在 Internet Explorer 8 中，相容性檢視變更瀏覽器如何解讀以 CSS、HTML 和檔物件模型 (DOM) 撰寫的程式碼，以嘗試符合 Internet Explorer 7。</span><span class="sxs-lookup"><span data-stu-id="2fc81-105">In Internet Explorer 8, Compatibility View changes how the browser interprets code that is written in CSS, HTML, and the Document Object Model (DOM) to try to match Internet Explorer 7.</span></span> <span data-ttu-id="2fc81-106">使用者在 Internet Explorer 8 相容性檢視中所觀看的網站，與使用者在 Internet Explorer 7 中所流覽的網站幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="2fc81-106">A site that a user views in Internet Explorer 8 Compatibility View is almost identical to a site that the user views in Internet Explorer 7.</span></span> <span data-ttu-id="2fc81-107">不過，相容性檢視不會變更瀏覽器解讀所有程式碼的方式。</span><span class="sxs-lookup"><span data-stu-id="2fc81-107">However, Compatibility View does not change how the browser interprets all code.</span></span> <span data-ttu-id="2fc81-108">例如，在 Internet Explorer 8 中，瀏覽器如何處理 ActiveX、剖析器、AJAX、JavaScript、網路和安全性的變更可能仍會造成相容性問題。</span><span class="sxs-lookup"><span data-stu-id="2fc81-108">For example, the changes in Internet Explorer 8 for how the browser handles ActiveX, the parser, AJAX, JavaScript, networking, and security might still cause compatibility issues.</span></span> <span data-ttu-id="2fc81-109">相容性檢視不會變更這些行為。</span><span class="sxs-lookup"><span data-stu-id="2fc81-109">Compatibility View does not change these behaviors.</span></span>

<span data-ttu-id="2fc81-110">在企業環境中，某些區域對於相容性問題的風險較低。</span><span class="sxs-lookup"><span data-stu-id="2fc81-110">In an enterprise environment, some areas have lower risk for compatibility issues.</span></span> <span data-ttu-id="2fc81-111">例如，內部網路區域網站預設會使用相容性檢視。</span><span class="sxs-lookup"><span data-stu-id="2fc81-111">For example, Intranet Zone websites use Compatibility View by default.</span></span> <span data-ttu-id="2fc81-112">使用網頁瀏覽器控制項轉譯的用戶端 web 應用程式，或 WebOC (Internet Explorer 轉譯引擎) ，對於相容性問題也有很低的風險，因為 Internet Explorer 8 預設為 WebOC 的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="2fc81-112">Client web applications that render by using the Web Browser Control, or the WebOC (Internet Explorer rendering engine), also have a low risk for compatibility issues because Internet Explorer 8 defaults to a compatibility mode for the WebOC.</span></span> <span data-ttu-id="2fc81-113">不過，相容性檢視的預設設定可能無法確保完全相容。</span><span class="sxs-lookup"><span data-stu-id="2fc81-113">However, the default configuration settings for Compatibility View might not ensure complete compatibility.</span></span> <span data-ttu-id="2fc81-114">若要判斷網站或 web 應用程式是否與 Internet Explorer 8 相容，您應該測試網站或 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="2fc81-114">To determine if a website or web application is compatible with Internet Explorer 8, you should test the website or web application.</span></span>

<span data-ttu-id="2fc81-115">如需 Internet Explorer 8 相容性檢視與 Internet Explorer 7 之間差異的詳細資訊，請參閱 [網站相容性和 Internet Explorer 8 的 blog](/archive/blogs/ie/site-compatibility-and-ie8)。</span><span class="sxs-lookup"><span data-stu-id="2fc81-115">For more information about the differences between Internet Explorer 8 Compatibility View and Internet Explorer 7, see the [Site Compatibility and Internet Explorer 8 blog](/archive/blogs/ie/site-compatibility-and-ie8).</span></span> <span data-ttu-id="2fc81-116">如需升級至 Internet Explorer 8 時要檢查的事項清單，請參閱 [Internet Explorer 8 準備工具](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx)組。</span><span class="sxs-lookup"><span data-stu-id="2fc81-116">For a list of what to check when you upgrade to Internet Explorer 8, see the [Internet Explorer 8 Readiness Toolkit](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).</span></span>

<span data-ttu-id="2fc81-117">如需相容性檢視的詳細資訊，請參閱 [Internet Explorer Team Blog](/archive/blogs/ie/)。</span><span class="sxs-lookup"><span data-stu-id="2fc81-117">For more information about Compatibility View, see the [Internet Explorer Team Blog](/archive/blogs/ie/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fc81-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fc81-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc81-119">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="2fc81-119">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
