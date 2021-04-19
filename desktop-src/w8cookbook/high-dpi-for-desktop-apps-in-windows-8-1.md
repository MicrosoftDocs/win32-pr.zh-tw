---
title: 適用于桌面應用程式的高 DPI Windows 8。1
description: 適用于桌面應用程式的高 DPI Windows 8。1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966871"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="2d8e9-103">適用于桌面應用程式的高 DPI Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="2d8e9-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="2d8e9-104">平台</span><span class="sxs-lookup"><span data-stu-id="2d8e9-104">Platforms</span></span>

<dl> <span data-ttu-id="2d8e9-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="2d8e9-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="2d8e9-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2d8e9-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="2d8e9-107">Description</span><span class="sxs-lookup"><span data-stu-id="2d8e9-107">Description</span></span>

<span data-ttu-id="2d8e9-108">在 Windows 8.1 的桌面應用程式中，除了100%、125% 和150% 調整（Windows 8 支援）之外，還會在顯示時執行200% 的縮放。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="2d8e9-109">此外，桌面應用程式會以個別監視器為基礎進行調整，而不是針對套用至所有顯示器的單一縮放比例進行縮放。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="2d8e9-110">開發人員也可以在 Windows 8.1 中呼叫新的 Api，以取得個別監視器規模的因素。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="2d8e9-111">表現</span><span class="sxs-lookup"><span data-stu-id="2d8e9-111">Manifestations</span></span>

<span data-ttu-id="2d8e9-112">使用者可以使用新的高密度顯示器搭配 Windows 8.1，取得利用較高圖元資料的絕佳視覺體驗。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="2d8e9-113">如果應用程式不會處理高 DPI，Windows 會將其調整為使用者。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="2d8e9-114">此外，使用者也可以在同一部電腦上混用高與低密度的組合，而 Windows 會適當地為每個顯示器調整內容規模。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="2d8e9-115">這是 Windows 8 的改進，其中的內容在某些顯示器上可能太大。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="2d8e9-116">降低</span><span class="sxs-lookup"><span data-stu-id="2d8e9-116">Mitigation</span></span>

<span data-ttu-id="2d8e9-117">由於 Windows 會調整不會自行擴充的應用程式，因此開發人員通常不需要執行額外的工作，但投資撰寫支援高 DPI 應用程式的開發人員會有競爭優勢，因為這些應用程式在新的高 DPI 膝上型電腦和桌上型電腦上看起來會更好。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="2d8e9-118">解決方法</span><span class="sxs-lookup"><span data-stu-id="2d8e9-118">Solution</span></span>

<span data-ttu-id="2d8e9-119">製作可利用高 DPI 的應用程式，是一項複雜的設計和執行工作。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="2d8e9-120">請參閱下列連結以取得教學課程資訊、建立簡報內容和類似的支援。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="2d8e9-121">測試</span><span class="sxs-lookup"><span data-stu-id="2d8e9-121">Tests</span></span>

<span data-ttu-id="2d8e9-122">即使開發人員未選擇讓應用程式使用高 DPI，也應在100%、125%、150% 和200% 的調整中測試其應用程式，以確保使用者體驗能獲得滿意且具競爭力。</span><span class="sxs-lookup"><span data-stu-id="2d8e9-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="2d8e9-123">資源</span><span class="sxs-lookup"><span data-stu-id="2d8e9-123">Resources</span></span>

-   [<span data-ttu-id="2d8e9-124">Windows 8.1 中的高 DPI 白皮書和教學課程</span><span class="sxs-lookup"><span data-stu-id="2d8e9-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="2d8e9-125">Windows 桌面範例程式</span><span class="sxs-lookup"><span data-stu-id="2d8e9-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="2d8e9-126">Windows 8.1 中的高 DPI 組建2013細分會話</span><span class="sxs-lookup"><span data-stu-id="2d8e9-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 