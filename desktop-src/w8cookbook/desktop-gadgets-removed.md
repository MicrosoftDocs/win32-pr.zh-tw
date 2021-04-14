---
title: 已移除桌面小工具
description: 已移除桌面小工具
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- 小工具
- 桌面小工具
- Windows 資訊看板
- 資訊看板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383041"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="7a8d3-107">已移除桌面小工具</span><span class="sxs-lookup"><span data-stu-id="7a8d3-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="7a8d3-108">平台</span><span class="sxs-lookup"><span data-stu-id="7a8d3-108">Platforms</span></span>

 <span data-ttu-id="7a8d3-109">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a8d3-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="7a8d3-110">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a8d3-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="7a8d3-111">Description</span><span class="sxs-lookup"><span data-stu-id="7a8d3-111">Description</span></span>

<span data-ttu-id="7a8d3-112">從功能的觀點來看，小工具已被取代，並由新的動態磚和應用程式 outclassed。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="7a8d3-113">小工具也會對使用者帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="7a8d3-114">作為平臺，有弱點存在，甚至可能會惡意探索無害的小工具。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="7a8d3-115">因此，為了將 Windows 8 保持在最新且安全的作業系統，我們選擇完全移除作業系統中的小工具。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="7a8d3-116">具有桌面上小工具的 Windows 7 使用者將會收到通知，並將會卸載小工具。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7a8d3-117">表現</span><span class="sxs-lookup"><span data-stu-id="7a8d3-117">Manifestation</span></span>

<span data-ttu-id="7a8d3-118">桌面小工具將無法在 Windows 桌面上使用。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7a8d3-119">降低</span><span class="sxs-lookup"><span data-stu-id="7a8d3-119">Mitigation</span></span>

<span data-ttu-id="7a8d3-120">桌面小工具 API 和資料夾結構將保留 Windows 8 的位置。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="7a8d3-121">使用此 API 以程式設計方式安裝和執行小工具的應用程式將會繼續執行，而不會 (失敗，但小工具本身將不會) 。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="7a8d3-122">解決方法</span><span class="sxs-lookup"><span data-stu-id="7a8d3-122">Solution</span></span>

<span data-ttu-id="7a8d3-123">桌面應用程式開發人員不應該在其安裝程式中封裝小工具。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="7a8d3-124">這些小工具會佔用空間給使用者，而且將無法在系統中執行。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="7a8d3-125">測試</span><span class="sxs-lookup"><span data-stu-id="7a8d3-125">Tests</span></span>

<span data-ttu-id="7a8d3-126">開發人員可以在 Windows 7 中停用桌面小工具的選用元件，以測試這項變更的相容性。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="7a8d3-127">若要停用 Windows 7 電腦上的小工具，請依照下列步驟執行：</span><span class="sxs-lookup"><span data-stu-id="7a8d3-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="7a8d3-128">流覽以開啟或關閉主控台中的 [Windows 功能]。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="7a8d3-129">取消核取 [Windows 小工具平台] 旁的方塊。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="7a8d3-130">按一下 [確定]，並遵循任何其他螢幕上的指示。</span><span class="sxs-lookup"><span data-stu-id="7a8d3-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="7a8d3-131">資源</span><span class="sxs-lookup"><span data-stu-id="7a8d3-131">Resources</span></span>

[<span data-ttu-id="7a8d3-132">小工具中的弱點可能會允許遠端執行程式碼</span><span class="sxs-lookup"><span data-stu-id="7a8d3-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




