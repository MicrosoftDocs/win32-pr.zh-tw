---
title: Windows 動畫管理員
description: Windows 動畫管理員 (Windows 動畫) 啟用使用者介面元素的豐富動畫。
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows 動畫 Windows 動畫，入口網站
- Windows 動畫管理員 Windows 動畫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933361"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="d1b69-105">Windows 動畫管理員</span><span class="sxs-lookup"><span data-stu-id="d1b69-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="d1b69-106">目的</span><span class="sxs-lookup"><span data-stu-id="d1b69-106">Purpose</span></span>

<span data-ttu-id="d1b69-107">Windows 動畫管理員 (Windows 動畫) 啟用使用者介面元素的豐富動畫。</span><span class="sxs-lookup"><span data-stu-id="d1b69-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="d1b69-108">它的設計目的是簡化將動畫新增至應用程式使用者介面的程式，並讓開發人員能夠執行流暢、自然和互動式的動畫。</span><span class="sxs-lookup"><span data-stu-id="d1b69-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="d1b69-109">動畫架構會管理動畫的排程和執行。</span><span class="sxs-lookup"><span data-stu-id="d1b69-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="d1b69-110">它提供實用數學函式的程式庫，可用於指定一段時間的 UI 元素行為，也可讓開發人員執行提供其他行為的自訂函式。</span><span class="sxs-lookup"><span data-stu-id="d1b69-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="d1b69-111">Windows 動畫不會執行轉譯;它可用於任何圖形平台，包括 Direct2D、Direct3D 或 GDI +。</span><span class="sxs-lookup"><span data-stu-id="d1b69-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1b69-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="d1b69-112">In this section</span></span>



| <span data-ttu-id="d1b69-113">主題</span><span class="sxs-lookup"><span data-stu-id="d1b69-113">Topic</span></span>                                                                                   | <span data-ttu-id="d1b69-114">描述</span><span class="sxs-lookup"><span data-stu-id="d1b69-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b69-115">Windows 動畫開發指南</span><span class="sxs-lookup"><span data-stu-id="d1b69-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="d1b69-116">開發人員指南提供 Windows 動畫的總覽，並提供涵蓋基本動畫工作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="d1b69-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="d1b69-117">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="d1b69-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="d1b69-118">本節所包含的主題會提供 Windows 動畫管理員的參考規格。</span><span class="sxs-lookup"><span data-stu-id="d1b69-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="d1b69-119">Windows 動畫範例</span><span class="sxs-lookup"><span data-stu-id="d1b69-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="d1b69-120">本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1b69-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="d1b69-121">Windows 動畫詞彙</span><span class="sxs-lookup"><span data-stu-id="d1b69-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="d1b69-122">本詞彙包含使用 Windows 動畫管理員之開發人員感興趣的詞彙和縮寫。</span><span class="sxs-lookup"><span data-stu-id="d1b69-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="d1b69-123">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="d1b69-123">Developer audience</span></span>

<span data-ttu-id="d1b69-124">Windows 動畫的設計目的是要讓熟悉 COM、UI 程式設計概念和一般動畫概念的有經驗的 C/c + + 開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="d1b69-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d1b69-125">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="d1b69-125">Run-time requirements</span></span>

<span data-ttu-id="d1b69-126">Windows 動畫管理員是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="d1b69-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="d1b69-127">在 Windows Vista 上需要支援 Windows 動畫管理員的應用程式可以利用 Windows Vista 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="d1b69-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="d1b69-128">需要適用于 Windows Vista 的平臺更新的應用程式可 Windows Update 確認已安裝，或是下載並安裝在背景中（否則為）。</span><span class="sxs-lookup"><span data-stu-id="d1b69-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="d1b69-129">如需詳細資訊，請參閱 [關於 Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b69-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1b69-130">其他資源</span><span class="sxs-lookup"><span data-stu-id="d1b69-130">Additional resources</span></span>

-   <span data-ttu-id="d1b69-131">[Windows Scenic 動畫總覽](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (影片) </span><span class="sxs-lookup"><span data-stu-id="d1b69-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="d1b69-132">[在 Windows 7 中：動畫管理員深入探討和教學](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) 課程 (影片) </span><span class="sxs-lookup"><span data-stu-id="d1b69-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="d1b69-133">[Windows 動畫- (影片的 Advanced 主題](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/)) </span><span class="sxs-lookup"><span data-stu-id="d1b69-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="d1b69-134">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="d1b69-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="d1b69-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1b69-135">Related topics</span></span>

[<span data-ttu-id="d1b69-136">動畫總覽 ( .NET Framework) </span><span class="sxs-lookup"><span data-stu-id="d1b69-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)