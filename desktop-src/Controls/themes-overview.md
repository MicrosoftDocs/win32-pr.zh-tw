---
title: 視覺化樣式
description: 本節提供視覺化樣式的總覽，並說明如何設定您的應用程式來使用它們。
ms.assetid: 9b135ccb-5e36-4657-b79c-689201047430
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bb1f8ff84f2c9f4d268ec8b50f8e7688519ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021287"
---
# <a name="visual-styles"></a><span data-ttu-id="1082b-103">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="1082b-103">Visual Styles</span></span>

## <a name="purpose"></a><span data-ttu-id="1082b-104">目的</span><span class="sxs-lookup"><span data-stu-id="1082b-104">Purpose</span></span>

<span data-ttu-id="1082b-105">*視覺效果樣式* 會根據使用者選擇的主題來變更通用控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="1082b-105">*Visual styles* changes the appearance of common controls based on the theme chosen by the user.</span></span> <span data-ttu-id="1082b-106">在 Windows 8 之前，您必須特別將應用程式設定為使用視覺化樣式;否則，無論目前選取的主題為何，應用程式的通用控制項一律會以與 Windows 傳統主題相關聯的樣式轉譯。</span><span class="sxs-lookup"><span data-stu-id="1082b-106">Prior to Windows 8, you must specifically configure your application to use visual styles; otherwise, the application's common controls are always rendered in the style associated with the Windows Classic theme, regardless of the currently selected theme.</span></span> <span data-ttu-id="1082b-107">在 Windows 8 中，無法關閉視覺效果樣式、Windows 傳統模式不再存在，而且已修改高對比模式來使用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="1082b-107">In Windows 8, visual styles can't be turned off, Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span>

<span data-ttu-id="1082b-108">本節提供視覺化樣式的總覽，並說明如何設定您的應用程式來使用它們。</span><span class="sxs-lookup"><span data-stu-id="1082b-108">This section provides an overview of visual styles and explains how to configure your application to use them.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1082b-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="1082b-109">Developer audience</span></span>

<span data-ttu-id="1082b-110">視覺化樣式是設計來供 C/c + + 開發人員和 UI 設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="1082b-110">Visual styles are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="1082b-111">一般情況下，開發人員需要對 UI 程式設計概念、Windows API 程式設計和 Unicode 進行中等程度的瞭解。</span><span class="sxs-lookup"><span data-stu-id="1082b-111">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1082b-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="1082b-112">Run-time requirements</span></span>

<span data-ttu-id="1082b-113">Windows Vista 和更新版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1082b-113">Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="1082b-114">256-color 模式不支援視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="1082b-114">Visual Styles are not supported in 256-color mode.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="1082b-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="1082b-115">In this section</span></span>

-   [<span data-ttu-id="1082b-116">新功能</span><span class="sxs-lookup"><span data-stu-id="1082b-116">What's New</span></span>](what-s-new-for-windows-8.md)
-   [<span data-ttu-id="1082b-117">視覺化樣式總覽</span><span class="sxs-lookup"><span data-stu-id="1082b-117">Visual Styles Overview</span></span>](visual-styles-overview.md)
-   [<span data-ttu-id="1082b-118">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="1082b-118">Enabling Visual Styles</span></span>](cookbook-overview.md)
-   [<span data-ttu-id="1082b-119">使用視覺效果樣式搭配自訂和 Owner-Drawn 控制項</span><span class="sxs-lookup"><span data-stu-id="1082b-119">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>](using-visual-styles.md)
-   [<span data-ttu-id="1082b-120">支援高對比主題</span><span class="sxs-lookup"><span data-stu-id="1082b-120">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
-   [<span data-ttu-id="1082b-121">視覺化樣式參考</span><span class="sxs-lookup"><span data-stu-id="1082b-121">Visual Styles Reference</span></span>](uxctl-ref.md)

## <a name="related-topics"></a><span data-ttu-id="1082b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="1082b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1082b-123">主題檔案格式</span><span class="sxs-lookup"><span data-stu-id="1082b-123">Theme File Format</span></span>](themesfileformat-overview.md)
</dt> <dt>

[<span data-ttu-id="1082b-124">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="1082b-124">Windows Controls</span></span>](window-controls.md)
</dt> </dl>

 

 




