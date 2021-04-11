---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: 開始使用 DirectX 圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026834"
---
# <a name="getting-started-with-directx-graphics"></a><span data-ttu-id="5aa59-103">開始使用 DirectX 圖形</span><span class="sxs-lookup"><span data-stu-id="5aa59-103">Getting started with DirectX Graphics</span></span>

<span data-ttu-id="5aa59-104">Microsoft DirectX 圖形提供一組 Api，可讓您用來建立遊戲和其他高效能的多媒體應用程式。</span><span class="sxs-lookup"><span data-stu-id="5aa59-104">Microsoft DirectX graphics provides a set of APIs that you can use to create games and other high-performance multimedia applications.</span></span> <span data-ttu-id="5aa59-105">DirectX 圖形包含高效能的2D 和3D 圖形支援。</span><span class="sxs-lookup"><span data-stu-id="5aa59-105">DirectX graphics includes support for high-performance 2-D and 3-D graphics.</span></span>

<span data-ttu-id="5aa59-106">若是立體圖形，請使用 Microsoft Direct3D 11 API。</span><span class="sxs-lookup"><span data-stu-id="5aa59-106">For 3-D graphics, use the Microsoft Direct3D 11 API.</span></span> <span data-ttu-id="5aa59-107">即使您有 Microsoft Direct3D 9 層級或 Microsoft Direct3D 10 層級的硬體，您也可以使用 Direct3D 11 API 並將目標設為 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 或功能層級 10 \_ x 裝置。</span><span class="sxs-lookup"><span data-stu-id="5aa59-107">Even if you have Microsoft Direct3D 9-level or Microsoft Direct3D 10-level hardware, you can use the Direct3D 11 API and target a [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x or feature level 10\_x device.</span></span> <span data-ttu-id="5aa59-108">如需有關如何使用 DirectX 開發3D 圖形的詳細資訊，請參閱 [使用 Directx 建立3d 圖形](/previous-versions/windows/apps/hh465137(v=win.10)
)。</span><span class="sxs-lookup"><span data-stu-id="5aa59-108">For info about how to develop 3-D graphics with DirectX, see [Create 3D graphics with DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span></span>

<span data-ttu-id="5aa59-109">若是2D 圖形和文字，請使用 Direct2D 和 [DirectWrite](./directwrite/direct-write-portal.md) ，而不是 Windows 圖形裝置介面 (GDI) 。</span><span class="sxs-lookup"><span data-stu-id="5aa59-109">For 2-D graphics and text, use Direct2D and [DirectWrite](./directwrite/direct-write-portal.md) rather than Windows Graphics Device Interface (GDI).</span></span>

<span data-ttu-id="5aa59-110">若要撰寫 Direct3D 11 或 Direct2D 填入的點陣圖，請使用 [DirectComposition](./directcomp/directcomposition-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="5aa59-110">To compose bitmaps that Direct3D 11 or Direct2D populated, use [DirectComposition](./directcomp/directcomposition-portal.md).</span></span>

<span data-ttu-id="5aa59-111">若要瞭解如何建立使用 DirectX 的 Windows Store 應用程式，請參閱 [使用 Directx 建立您的第一個 Windows store 應用程式](/previous-versions/windows/apps/br229580(v=win.10)
)。</span><span class="sxs-lookup"><span data-stu-id="5aa59-111">To learn about how to create a Windows Store app that uses DirectX, see [Create your first Windows Store app using DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span></span> <span data-ttu-id="5aa59-112">您可以使用 [**Windows. UI：： Xaml：： Controls：： SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) 類別來建立具有 Xaml UI 覆迭的高效能 DirectX 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5aa59-112">You can use the [**Windows.UI::Xaml::Controls::SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) class to create high-performance DirectX apps with a XAML UI overlay.</span></span> <span data-ttu-id="5aa59-113">如需在 Windows 應用程式中結合 XAML 和 DirectX 的詳細資訊，請參閱 [DirectX 和 XAML interop](/previous-versions/windows/apps/hh825871(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="5aa59-113">For more info about combining XAML and DirectX in a Windows app, see [DirectX and XAML interop](/previous-versions/windows/apps/hh825871(v=win.10)).</span></span>

<span data-ttu-id="5aa59-114">若要瞭解如何建立 Windows 8 的顯示驅動程式，請參閱 [Windows 顯示驅動程式模型的藍圖 (WDDM) ](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo)。</span><span class="sxs-lookup"><span data-stu-id="5aa59-114">To learn about how to build a display driver for Windows 8, see [Roadmap for the Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span></span>

<span data-ttu-id="5aa59-115">如果您需要先前 DirectX 版本的檔，請參閱 [傳統 Directx 圖形](/windows/desktop/classic-directx-graphics)。</span><span class="sxs-lookup"><span data-stu-id="5aa59-115">If you need the documentation for previous DirectX versions, see [Classic DirectX Graphics](/windows/desktop/classic-directx-graphics).</span></span>


 

 
