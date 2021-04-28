---
description: 使用者介面 - 高 DPI 感知
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 使用者介面 - 高 DPI 感知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116066"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="57b7a-103">使用者介面 - 高 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="57b7a-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="57b7a-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="57b7a-104">Affected Platforms</span></span>

 <span data-ttu-id="57b7a-105">**客戶** 端-windows XP \| windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="57b7a-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="57b7a-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="57b7a-106">Feature Impact</span></span>

<span data-ttu-id="57b7a-107">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="57b7a-107">**Severity** - Medium</span></span>  
<span data-ttu-id="57b7a-108">**頻率** -中型</span><span class="sxs-lookup"><span data-stu-id="57b7a-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="57b7a-109">Description</span><span class="sxs-lookup"><span data-stu-id="57b7a-109">Description</span></span>

<span data-ttu-id="57b7a-110">目標是鼓勵終端使用者將其顯示器設為原生解析度，並使用 DPI 而非螢幕解析度來變更顯示文字和影像的大小。</span><span class="sxs-lookup"><span data-stu-id="57b7a-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="57b7a-111">在 Oem 設定的電腦上，Windows 7 可以自動偵測並設定全新的 DPI，以使用 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="57b7a-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="57b7a-112">您可以使用一些工具來協助設計高度 DPI 感知的應用程式，以確保最容易閱讀的結果。</span><span class="sxs-lookup"><span data-stu-id="57b7a-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="57b7a-113">我們已將兩個新的高 DPI 功能新增至 Windows 7：</span><span class="sxs-lookup"><span data-stu-id="57b7a-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="57b7a-114">每個使用者的 DPI 設定 (先前每一部電腦) </span><span class="sxs-lookup"><span data-stu-id="57b7a-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="57b7a-115">在不重新開機 (登出/登入的情況下，仍需要變更 DPI) </span><span class="sxs-lookup"><span data-stu-id="57b7a-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="57b7a-116">影響的表現</span><span class="sxs-lookup"><span data-stu-id="57b7a-116">Manifestation of Impact</span></span>

<span data-ttu-id="57b7a-117">未處理高 DPI 案例的應用程式可能會顯示視覺構件，包括：</span><span class="sxs-lookup"><span data-stu-id="57b7a-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="57b7a-118">由其他 UI 元素剪切 UI 或文字</span><span class="sxs-lookup"><span data-stu-id="57b7a-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="57b7a-119">不一致的字型大小</span><span class="sxs-lookup"><span data-stu-id="57b7a-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="57b7a-120">螢幕 Ui</span><span class="sxs-lookup"><span data-stu-id="57b7a-120">Off-screen UIs</span></span>
-   <span data-ttu-id="57b7a-121">文字或 UI 的模糊</span><span class="sxs-lookup"><span data-stu-id="57b7a-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="57b7a-122">中斷的拖放或其他輸入</span><span class="sxs-lookup"><span data-stu-id="57b7a-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="57b7a-123">全螢幕的 DX 應用程式呈現部分關閉畫面</span><span class="sxs-lookup"><span data-stu-id="57b7a-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="57b7a-124">解決方法</span><span class="sxs-lookup"><span data-stu-id="57b7a-124">Solution</span></span>

<span data-ttu-id="57b7a-125">將您的應用程式設為 DPI 感知：</span><span class="sxs-lookup"><span data-stu-id="57b7a-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="57b7a-126">執行高階功能測試階段，包括在下列設定中安裝和卸載：</span><span class="sxs-lookup"><span data-stu-id="57b7a-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="57b7a-127">設定</span><span class="sxs-lookup"><span data-stu-id="57b7a-127">Setting</span></span>                                              | <span data-ttu-id="57b7a-128">應該檢查哪些狀況</span><span class="sxs-lookup"><span data-stu-id="57b7a-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="57b7a-129">1024 @ 120 DPI (125% 調整) </span><span class="sxs-lookup"><span data-stu-id="57b7a-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="57b7a-130">這是 ~ 800x600 的有效解析度，因此請尋找在螢幕或版面配置問題中裁剪的 UI。</span><span class="sxs-lookup"><span data-stu-id="57b7a-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="57b7a-131">也請尋找晃動點陣圖 & 圖示。</span><span class="sxs-lookup"><span data-stu-id="57b7a-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="57b7a-132">1600x1200 @144 DPI (150% 調整) </span><span class="sxs-lookup"><span data-stu-id="57b7a-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="57b7a-133">模糊的 UI。</span><span class="sxs-lookup"><span data-stu-id="57b7a-133">Blurry UI.</span></span> <span data-ttu-id="57b7a-134">確認所有的滑鼠作業都能正常運作，尤其是拖曳 & drop 作業。</span><span class="sxs-lookup"><span data-stu-id="57b7a-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="57b7a-135">也請確認全螢幕模式是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="57b7a-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="57b7a-136">已停用 DPI 虛擬化的 1600x1200 @ 144 DPI</span><span class="sxs-lookup"><span data-stu-id="57b7a-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="57b7a-137">按鈕和 UI 通常不會與較大的文字相對應，& 將會有大量的文字裁剪。</span><span class="sxs-lookup"><span data-stu-id="57b7a-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="57b7a-138">尋找一般 & 晃動 bitmats & 圖示的版面配置問題。</span><span class="sxs-lookup"><span data-stu-id="57b7a-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="57b7a-139">寫下所有找到的問題，包括位置、螢幕解析度和 DPI 設定，以及應用程式在其他 DPI/解析度設定中的行為，以達到完整性</span><span class="sxs-lookup"><span data-stu-id="57b7a-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="57b7a-140">針對常見的 DPI 編碼問題檢查每個問題</span><span class="sxs-lookup"><span data-stu-id="57b7a-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="57b7a-141">評估讓應用程式完全 DPI 感知的成本</span><span class="sxs-lookup"><span data-stu-id="57b7a-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="57b7a-142">建立所需的高 DPI 資產清單 (例如按鈕、圖示) </span><span class="sxs-lookup"><span data-stu-id="57b7a-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="57b7a-143">完成步驟1中找到的 DPI 問題清單並加以修正</span><span class="sxs-lookup"><span data-stu-id="57b7a-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="57b7a-144">整合步驟5中的新資產</span><span class="sxs-lookup"><span data-stu-id="57b7a-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="57b7a-145">宣告您的應用程式 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="57b7a-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="57b7a-146">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="57b7a-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="57b7a-147">重新執行 DPI 感知評量，並確認問題已修正。</span><span class="sxs-lookup"><span data-stu-id="57b7a-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="57b7a-148">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="57b7a-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="57b7a-149">Windows 上的高 DPI 桌面應用程式開發</span><span class="sxs-lookup"><span data-stu-id="57b7a-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="57b7a-150">**接觸技術問題：**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="57b7a-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
