---
title: 限制
description: 限制
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- Windows 上的 OpenGL，限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672683"
---
# <a name="limitations"></a><span data-ttu-id="f908d-104">限制</span><span class="sxs-lookup"><span data-stu-id="f908d-104">Limitations</span></span>

<span data-ttu-id="f908d-105">泛型實有下列限制：</span><span class="sxs-lookup"><span data-stu-id="f908d-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="f908d-106">列印：</span><span class="sxs-lookup"><span data-stu-id="f908d-106">Printing.</span></span>

    <span data-ttu-id="f908d-107">您只能使用中繼檔將 OpenGL 影像直接列印到印表機。</span><span class="sxs-lookup"><span data-stu-id="f908d-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="f908d-108">如需詳細資訊，請參閱 [列印 OpenGL 映射](printing-an-opengl-image.md)。</span><span class="sxs-lookup"><span data-stu-id="f908d-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="f908d-109">在雙重緩衝的視窗中，無法混合 OpenGL 和 GDI 圖形。</span><span class="sxs-lookup"><span data-stu-id="f908d-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="f908d-110">應用程式可以將 OpenGL 圖形和 GDI 圖形直接繪製成單一緩衝視窗，但不能直接繪製到雙重緩衝視窗。</span><span class="sxs-lookup"><span data-stu-id="f908d-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="f908d-111">沒有每個視窗的硬體色彩調色板。</span><span class="sxs-lookup"><span data-stu-id="f908d-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="f908d-112">Windows 具有單一系統硬體調色板，適用于整個畫面。</span><span class="sxs-lookup"><span data-stu-id="f908d-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="f908d-113">OpenGL 視窗不能有自己的硬體調色板，但可以有自己的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="f908d-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="f908d-114">若要這樣做，它必須變成可辨識元件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f908d-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="f908d-115">如需詳細資訊，請參閱 [OpenGL 色彩模式和 Windows 調色板管理](opengl-color-modes-and-windows-palette-management.md)。</span><span class="sxs-lookup"><span data-stu-id="f908d-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="f908d-116">不直接支援剪貼簿、動態資料交換 (DDE) 或 OLE。</span><span class="sxs-lookup"><span data-stu-id="f908d-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="f908d-117">具有 OpenGL 圖形的視窗不直接支援這些 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="f908d-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="f908d-118">不過，有一些因應措施可使用剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="f908d-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="f908d-119">如需詳細資訊，請參閱 [將 OpenGL 影像複製到剪貼](copying-an-opengl-image-to-the-clipboard.md)簿。</span><span class="sxs-lookup"><span data-stu-id="f908d-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="f908d-120">不包含發明者 2.0 c + + 類別庫。</span><span class="sxs-lookup"><span data-stu-id="f908d-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="f908d-121">發明者類別庫建置於 OpenGL 之上，可提供更高層級的程式設計3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="f908d-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="f908d-122">它並未包含在目前版本的適用于 Windows 的 OpenGL 中。</span><span class="sxs-lookup"><span data-stu-id="f908d-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="f908d-123">下列像素格式功能不支援： stereoscopic 影像、Alpha bitplanes 和輔助緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f908d-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="f908d-124">不過，也支援數個附屬緩衝區，包括：樣板緩衝區、累積緩衝區、背景緩衝區 (雙緩衝) 、重迭和基礎平面緩衝區，以及深度 (Z 軸) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f908d-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




