---
title: Direct2D 範例
description: 下列範例示範 Direct2D API。
ms.assetid: 4e972beb-5c69-4617-a5fe-0e0e4759240a
keywords:
- Direct2D，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4219d5b10a6a46659fc0c13ac091a2f3ab01b2c
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/07/2020
ms.locfileid: "103932995"
---
# <a name="direct2d-samples"></a><span data-ttu-id="aac94-104">Direct2D 範例</span><span class="sxs-lookup"><span data-stu-id="aac94-104">Direct2D samples</span></span>

<span data-ttu-id="aac94-105">下列範例示範 Direct2D API。</span><span class="sxs-lookup"><span data-stu-id="aac94-105">The following samples demonstrate the Direct2D API.</span></span>

## <a name="windows-10-and-microsoft-visual-studio-2015-samples"></a><span data-ttu-id="aac94-106">Windows 10 和 Microsoft Visual Studio 2015 範例</span><span class="sxs-lookup"><span data-stu-id="aac94-106">Windows 10 and Microsoft Visual Studio 2015 samples</span></span>

| <span data-ttu-id="aac94-107">範例</span><span class="sxs-lookup"><span data-stu-id="aac94-107">Sample</span></span> | <span data-ttu-id="aac94-108">描述</span><span class="sxs-lookup"><span data-stu-id="aac94-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="aac94-109">Direct2D 自訂影像效果範例</span><span class="sxs-lookup"><span data-stu-id="aac94-109">Direct2D custom image effects sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) | <span data-ttu-id="aac94-110">此範例示範如何使用 HLSL 圖元、頂點和計算著色器來執行 [自訂效果](custom-effects.md) 。</span><span class="sxs-lookup"><span data-stu-id="aac94-110">This sample demonstrates how to implement [Custom effects](custom-effects.md) using HLSL pixel, vertex, and compute shaders.</span></span> |
| [<span data-ttu-id="aac94-111">Direct2D 漸層網格範例</span><span class="sxs-lookup"><span data-stu-id="aac94-111">Direct2D gradient mesh sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh) | <span data-ttu-id="aac94-112">這個範例示範如何在 Direct2D 中具現化和轉譯漸層網格。</span><span class="sxs-lookup"><span data-stu-id="aac94-112">This sample demonstrates how to instantiate and render a gradient mesh in Direct2D.</span></span> <span data-ttu-id="aac94-113">此範例會使用 Direct2D 所提供的 helper 方法來建立包含兩個 tensor 修補程式（共用一側）的網格。</span><span class="sxs-lookup"><span data-stu-id="aac94-113">This samples uses the helper method provided by Direct2D to create a mesh consisting of two tensor patches that share a side.</span></span> |
| [<span data-ttu-id="aac94-114">Direct2D 相片調整範例</span><span class="sxs-lookup"><span data-stu-id="aac94-114">Direct2D photo adjustment sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment) | <span data-ttu-id="aac94-115">此範例示範如何使用 Direct2D 和 Direct2D 效果來建立相片檢視器和編輯器。</span><span class="sxs-lookup"><span data-stu-id="aac94-115">This sample demonstrates how to build a photo viewer and editor using Direct2D and Direct2D Effects.</span></span> |

## <a name="windows-8-and-microsoft-visual-studio-2013-samples"></a><span data-ttu-id="aac94-116">Windows 8 和 Microsoft Visual Studio 2013 範例</span><span class="sxs-lookup"><span data-stu-id="aac94-116">Windows 8 and Microsoft Visual Studio 2013 samples</span></span>

| | |
|-|-|
| [<span data-ttu-id="aac94-117">Direct2D 複合效果模式範例</span><span class="sxs-lookup"><span data-stu-id="aac94-117">Direct2D composite effect modes sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample) | <span data-ttu-id="aac94-118">這個範例會顯示 Direct2D 中可用的各種複合和 blend 模式範圍。</span><span class="sxs-lookup"><span data-stu-id="aac94-118">This sample shows the wide range of composite and blend modes available from Direct2D.</span></span> |
| [<span data-ttu-id="aac94-119">Direct2D 基本影像效果範例</span><span class="sxs-lookup"><span data-stu-id="aac94-119">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample) | <span data-ttu-id="aac94-120">這個範例示範如何載入影像、對它套用高斯模糊效果，然後將它顯示在 Windows：： UI：： Core：： CoreWindow 中。</span><span class="sxs-lookup"><span data-stu-id="aac94-120">This sample shows how to load an image, apply the Gaussian blur effect to it, and then display it in a Windows::UI::Core::CoreWindow.</span></span> |
| [<span data-ttu-id="aac94-121">Direct2D 和 WIC 範例中的 JPEG YCbCr 優化</span><span class="sxs-lookup"><span data-stu-id="aac94-121">JPEG YCbCr optimizations in Direct2D and WIC sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) | <span data-ttu-id="aac94-122">示範 Direct2D 中的效能優化，以及原生 JPEG YCbCr 格式的 Windows 影像處理元件呈現影像資料。</span><span class="sxs-lookup"><span data-stu-id="aac94-122">Demonstrates performance optimizations in Direct2D and the Windows Imaging Component rendering image data in the JPEG YCbCr format natively.</span></span> |
| [<span data-ttu-id="aac94-123">DirectX 明信片應用程式範例</span><span class="sxs-lookup"><span data-stu-id="aac94-123">DirectX postcard app sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20postcard%20app%20sample) | <span data-ttu-id="aac94-124">此範例示範如何使用 DirectX 搭配 c + + 的端對端執行，以利用 DirectX 和 XAML interop 來建立明信片。</span><span class="sxs-lookup"><span data-stu-id="aac94-124">This sample demonstrates the end-to-end implementation of a simple Windows Store app using DirectX with C++ for postcard creation using DirectX and XAML interop.</span></span> |