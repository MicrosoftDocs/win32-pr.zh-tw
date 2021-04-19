---
title: 關於 Windows Color System 版本1。0
description: 關於 Windows Color System 版本1。0
ms.assetid: 2a162840-660e-4a66-ad16-ef3c9b07925e
keywords:
- Windows Color System (WCS) ，關於
- WCS (Windows 色彩系統) ，關於
- '影像色彩管理、Windows 色彩系統 (WCS) '
- '色彩管理、Windows 色彩系統 (WCS) '
- '色彩、Windows 色彩系統 (WCS) '
- 影像色彩管理 (ICM)
- 'ICM (影像色彩管理) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad2673f8b0943e16a1fbbacde11c4469d00b4e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106981062"
---
# <a name="about-windows-color-system-version-10"></a><span data-ttu-id="1ca61-110">關於 Windows Color System 版本1。0</span><span class="sxs-lookup"><span data-stu-id="1ca61-110">About Windows Color System Version 1.0</span></span>

<span data-ttu-id="1ca61-111">Microsoft Windows Color System (WCS) 技術可確保色彩影像、圖形或文字物件在任何裝置上都能盡可能接近其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。</span><span class="sxs-lookup"><span data-stu-id="1ca61-111">Microsoft Windows Color System (WCS) technology ensures that a color image, graphic or text object is rendered as close as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="1ca61-112">無論您是掃描彩色掃描器上的影像或其他圖形、透過網際網路進行下載、在螢幕上進行觀看或編輯，或是將它輸出到紙張、電影或其他媒體，WCS 1.0 都能協助您保持其色彩一致且正確。</span><span class="sxs-lookup"><span data-stu-id="1ca61-112">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it on the screen, or outputting it to paper, film, or other media, WCS 1.0 helps you keep its colors consistent and accurate.</span></span>

<span data-ttu-id="1ca61-113">WCS 1.0 是 Microsoft Windows 不可或缺的一部分，因為 WCS 1.0 以一組 WIN32 API 函式的形式內建在 Windows 系列的作業系統中，因此可供任何應用程式、設備磁碟機、裝置校正工具或色彩管理模組 (的 CMM) 。</span><span class="sxs-lookup"><span data-stu-id="1ca61-113">WCS 1.0 is an integral part of Microsoft Windows Because WCS 1.0 is built into the Windows family of operating systems as a set of Win32 API functions, it is readily available to any application, device driver, device calibration tool, or color management module (CMM).</span></span>

<span data-ttu-id="1ca61-114">映射色彩管理的版本 1.0 (ICM) 已在 Microsoft Windows 95 中提供，並在 Windows 裝置內容中提供基本的色彩管理功能。</span><span class="sxs-lookup"><span data-stu-id="1ca61-114">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="1ca61-115">ICM 2.0 版包含在 Windows 98、Windows Millennium Edition、Windows 2000 和 Windows XP 中，以及在裝置內容以外執行色彩管理的包含函式。</span><span class="sxs-lookup"><span data-stu-id="1ca61-115">ICM version 2.0 is included in Windows 98, Windows Millennium Edition, Windows 2000, and Windows XP and included functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="1ca61-116">這些函式適用于需求較高的色彩管理需求，並讓應用程式更能掌控色彩管理程式。</span><span class="sxs-lookup"><span data-stu-id="1ca61-116">These functions were suitable for more demanding color management requirements, and give applications greater control over the color-management process.</span></span>

<span data-ttu-id="1ca61-117">WCS 1.0 版包含在 Windows Vista 中，並包含各種新功能，可針對廠商的靈活、透明度、可預測性和 extensiblity 提供顯著的改進。</span><span class="sxs-lookup"><span data-stu-id="1ca61-117">WCS version 1.0 is included in Windows Vista and includes a variety of new functions that provides significant improvements in flexiblity, transparency, predictability and extensiblity for vendors.</span></span>

<span data-ttu-id="1ca61-118">使用 WCS 1.0 可受益于哪些類型的應用程式？</span><span class="sxs-lookup"><span data-stu-id="1ca61-118">What kinds of applications will benefit from using WCS 1.0?</span></span> <span data-ttu-id="1ca61-119">現今在 Windows Vista 環境中執行的應用程式幾乎都是如此。</span><span class="sxs-lookup"><span data-stu-id="1ca61-119">Almost any application running in a Windows Vista environment today.</span></span> <span data-ttu-id="1ca61-120">基本色彩管理功能已成為各種應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="1ca61-120">Basic color management capability is becoming a requirement for applications of all kinds.</span></span>

<span data-ttu-id="1ca61-121">過去幾年來，色彩顯示和列印已經過改良，現在可讓您不只是在桌上型電腦發行，也可以在各式各樣的資料和展示應用程式中使用相片實際色彩影像和複雜色彩圖形。</span><span class="sxs-lookup"><span data-stu-id="1ca61-121">Color display and printing have improved in recent years to the point where photo-realistic color images and complex color graphics are now commonly used not only in desktop publishing, but also across a broad spectrum of data and presentation applications.</span></span> <span data-ttu-id="1ca61-122">COM 和 ActiveX 這類物件技術在幾乎每一種資料空間中都有內嵌的色彩物件。</span><span class="sxs-lookup"><span data-stu-id="1ca61-122">Object technologies such as COM and ActiveX have embedded color objects in virtually every kind of data space.</span></span>

<span data-ttu-id="1ca61-123">服裝目錄、線上藝術、家族相片專輯、商務標誌、圖表、圖形、簡報、預覽列印和色彩模擬，都只是一些色彩重要的日常應用程式範例。</span><span class="sxs-lookup"><span data-stu-id="1ca61-123">Clothing catalogs, online art, family photo albums, business logos, charts, graphs, presentations, print previews, and color simulations are just a few examples of everyday applications where color matters.</span></span>

<span data-ttu-id="1ca61-124">因此，有越來越多的使用者要求其應用程式能夠正確地顯示色彩。</span><span class="sxs-lookup"><span data-stu-id="1ca61-124">As a result, more and more users are requiring their applications to be capable of accurate color display.</span></span> <span data-ttu-id="1ca61-125">色彩轉譯不良會毀損對使用者日益重要的影像和圖形。</span><span class="sxs-lookup"><span data-stu-id="1ca61-125">Poor color rendering ruins the images and graphics that are increasingly important to users.</span></span>

<span data-ttu-id="1ca61-126">在基本層級中，幾乎所有應用程式都應該能夠自動調整色彩，使其輸出在不同的監視器和印表機上看起來相同。</span><span class="sxs-lookup"><span data-stu-id="1ca61-126">On a fundamental level, almost any application should be able to adjust color automatically so that its output looks the same on different monitors and printers.</span></span> <span data-ttu-id="1ca61-127">WCS 1.0 提供一組函式來傳遞這種對使用者而言是透明的色彩管理，並且在應用程式中需要很少的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="1ca61-127">WCS 1.0 provides a set of functions to deliver this kind of color management that is transparent to a user and requires little overhead in the application.</span></span>

<span data-ttu-id="1ca61-128">在較高的層級上，WCS 1.0 會提供額外的功能，以提供更複雜且可控制的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="1ca61-128">On a higher level, WCS 1.0 provides additional functions that deliver more complex and controllable color management.</span></span> <span data-ttu-id="1ca61-129">圖形和桌上型電腦發佈應用程式需要這些額外的功能，讓使用者在整個生產過程中都能以一致的色彩在多部裝置之間精確地運作。</span><span class="sxs-lookup"><span data-stu-id="1ca61-129">Graphics and desktop publishing applications need these additional capabilities to let their users work precisely with consistent color across many devices throughout a production process.</span></span>

<span data-ttu-id="1ca61-130">一般情況下，如果軟體廠商的產品是以彩色的輸入或輸出和硬體廠商的顏色周邊來處理，就會發現 WCS 1.0 是簡化成功產品傳遞的關鍵技術。</span><span class="sxs-lookup"><span data-stu-id="1ca61-130">In general, software vendors whose products deal with color input or output and hardware vendors of color peripherals will find WCS 1.0 a key technology for simplifying the delivery of successful products.</span></span> <span data-ttu-id="1ca61-131">接下來的各節包括：</span><span class="sxs-lookup"><span data-stu-id="1ca61-131">The following sections include:</span></span>

-   [<span data-ttu-id="1ca61-132">WCS 1.0 版的新功能</span><span class="sxs-lookup"><span data-stu-id="1ca61-132">What's New in Version 1.0 of WCS</span></span>](what-s-new-in-version-1-0-of-wcs.md)
-   [<span data-ttu-id="1ca61-133">WCS 1.0 可用性</span><span class="sxs-lookup"><span data-stu-id="1ca61-133">WCS 1.0 Availability</span></span>](wcs-1-0-availability.md)

 

 




