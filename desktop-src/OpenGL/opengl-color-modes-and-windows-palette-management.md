---
title: OpenGL 色彩模式和 Windows 調色板管理
description: Microsoft 在 Windows 中執行 OpenGL 支援兩種色彩圖元資料模式的 RGBA 和色彩索引模式。 Windows 提供兩種類似的方式來處理色彩真色彩和調色板管理。
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- Windows 上的 OpenGL，色彩模式
- Windows 上的 OpenGL，調色板管理
- 調色板管理 OpenGL
- 色彩模式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300627"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a><span data-ttu-id="d67b2-108">OpenGL 色彩模式和 Windows 調色板管理</span><span class="sxs-lookup"><span data-stu-id="d67b2-108">OpenGL Color Modes and Windows Palette Management</span></span>

<span data-ttu-id="d67b2-109">Microsoft 在 Windows 中執行 OpenGL 支援兩種色彩圖元資料模式： RGBA 和色彩索引模式。</span><span class="sxs-lookup"><span data-stu-id="d67b2-109">The Microsoft implementation of OpenGL in Windows supports two color pixel data modes: RGBA and color-index modes.</span></span> <span data-ttu-id="d67b2-110">Windows 提供兩種類似的方式來處理色彩： true 色彩和調色板管理。</span><span class="sxs-lookup"><span data-stu-id="d67b2-110">Windows provide two analogous ways of handling color: true color and palette management.</span></span>

<span data-ttu-id="d67b2-111">若為真色彩裝置，每圖元可以接受16、24或更多位的色彩資訊，則可以同時顯示數十萬個、數十個或更多的色彩。</span><span class="sxs-lookup"><span data-stu-id="d67b2-111">True-color devices, able to accept 16, 24, or more bits of color information per pixel, can display tens of thousands, tens of millions, or more colors simultaneously.</span></span> <span data-ttu-id="d67b2-112">但是，當應用程式必須在選擇區類型的裝置上管理 RGBA 或色彩索引模式時，就會發生複雜性問題。</span><span class="sxs-lookup"><span data-stu-id="d67b2-112">Complexities arise, however, when an application has to manage RGBA or color-index mode on a palette-type device.</span></span> <span data-ttu-id="d67b2-113">選擇區類型的裝置（例如256色 VGA 顯示器）受限於可同時顯示的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="d67b2-113">Palette-type devices, such as a 256-color VGA display, are limited in the number of colors they can display simultaneously.</span></span> <span data-ttu-id="d67b2-114">應用程式必須處理一些複雜的詳細資料，才能成功使用多元件類型的裝置。</span><span class="sxs-lookup"><span data-stu-id="d67b2-114">Applications must handle a number of tricky details to successfully use palette-type devices.</span></span> <span data-ttu-id="d67b2-115">由於色彩索引模式程式並不會使用硬體選擇區，因此比起使用 RGBA 模式的程式更難搭配使用真實色彩裝置。</span><span class="sxs-lookup"><span data-stu-id="d67b2-115">Because color-index mode programs don't use a hardware palette, they are more difficult to use with true-color devices than programs using the RGBA mode.</span></span>

 

 




