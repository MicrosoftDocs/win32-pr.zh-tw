---
title: 放大 API
description: 放大 API 可讓應用程式放大整個螢幕或畫面的部分，並套用色彩效果。
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2020
ms.locfileid: "103841860"
---
# <a name="magnification-api"></a><span data-ttu-id="4ea77-103">放大 API</span><span class="sxs-lookup"><span data-stu-id="4ea77-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="4ea77-104">目的</span><span class="sxs-lookup"><span data-stu-id="4ea77-104">Purpose</span></span>

<span data-ttu-id="4ea77-105">放大 API 可讓應用程式放大整個螢幕或畫面的部分，並套用色彩效果。</span><span class="sxs-lookup"><span data-stu-id="4ea77-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4ea77-106">適用時</span><span class="sxs-lookup"><span data-stu-id="4ea77-106">Where applicable</span></span>

<span data-ttu-id="4ea77-107">藉由使用放大 API，開發人員可以建立以 Windows 為基礎的輔助技術應用程式，以放大螢幕並將色彩效果套用至放大的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="4ea77-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="4ea77-108">對於視力較低的使用者，放大的影像大小和色彩效果有助於讓電腦更容易查看和使用。</span><span class="sxs-lookup"><span data-stu-id="4ea77-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4ea77-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="4ea77-109">Developer audience</span></span>

<span data-ttu-id="4ea77-110">放大 API 主要是針對瞭解 Windows 程式設計的 C 和 c + + 開發人員，以及熟悉圖形程式設計概念的人員所設計。</span><span class="sxs-lookup"><span data-stu-id="4ea77-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4ea77-111">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="4ea77-111">Run-time requirements</span></span>

<span data-ttu-id="4ea77-112">在 Windows Vista 和更新版本的作業系統上，支援放大 API 的初始版本。</span><span class="sxs-lookup"><span data-stu-id="4ea77-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="4ea77-113">第二個版本新增了全螢幕放大功能，並支援 Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4ea77-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="4ea77-114">Magnification.dll 支援 API。</span><span class="sxs-lookup"><span data-stu-id="4ea77-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="4ea77-115">若要編譯您的應用程式，請包含放大和連結至放大程式庫。</span><span class="sxs-lookup"><span data-stu-id="4ea77-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="4ea77-116">在 WOW64 下不支援放大 API;也就是說，32位的放大鏡應用程式將無法在64位 Windows 上正確執行。</span><span class="sxs-lookup"><span data-stu-id="4ea77-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ea77-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="4ea77-117">In this section</span></span>

| <span data-ttu-id="4ea77-118">主題</span><span class="sxs-lookup"><span data-stu-id="4ea77-118">Topic</span></span> | <span data-ttu-id="4ea77-119">描述</span><span class="sxs-lookup"><span data-stu-id="4ea77-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="4ea77-120">放大 API 總覽</span><span class="sxs-lookup"><span data-stu-id="4ea77-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="4ea77-121">本主題說明放大 API，並說明如何在應用程式中使用它。</span><span class="sxs-lookup"><span data-stu-id="4ea77-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="4ea77-122">參考</span><span class="sxs-lookup"><span data-stu-id="4ea77-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="4ea77-123">本章節包含縮放 API 的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="4ea77-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="4ea77-124">範例</span><span class="sxs-lookup"><span data-stu-id="4ea77-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="4ea77-125">下列範例應用程式會示範如何使用放大 API 來建立放大整個畫面的全螢幕放大鏡，以及視窗中放大和顯示幕幕一部分的視窗放大鏡。</span><span class="sxs-lookup"><span data-stu-id="4ea77-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="4ea77-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ea77-126">Related topics</span></span>

<span data-ttu-id="4ea77-127">[Microsoft 協助工具網站](https://www.microsoft.com/accessibility/)， [Windows 10 的協助工具](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="4ea77-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
