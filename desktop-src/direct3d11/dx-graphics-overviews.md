---
title: Direct3D 11 程式設計指南
description: 程式設計指南包含如何使用 Microsoft Direct3D 11 程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。
ms.assetid: 1db500e4-c03d-442a-b429-1599d9591292
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb374d19126f46ed484154b363c975ca9ebe17
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316741"
---
# <a name="programming-guide-for-direct3d-11"></a><span data-ttu-id="0ffbe-103">Direct3D 11 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0ffbe-103">Programming guide for Direct3D 11</span></span>

<span data-ttu-id="0ffbe-104">程式設計指南包含如何使用 Microsoft Direct3D 11 程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-104">The programming guide contains information about how to use the Microsoft Direct3D 11 programmable pipeline to create realtime 3D graphics for games as well as scientific and desktop applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0ffbe-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="0ffbe-105">In this section</span></span>

| <span data-ttu-id="0ffbe-106">主題</span><span class="sxs-lookup"><span data-stu-id="0ffbe-106">Topic</span></span> | <span data-ttu-id="0ffbe-107">描述</span><span class="sxs-lookup"><span data-stu-id="0ffbe-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="0ffbe-108">裝置</span><span class="sxs-lookup"><span data-stu-id="0ffbe-108">Devices</span></span>](overviews-direct3d-11-devices.md) | <span data-ttu-id="0ffbe-109">本節說明 Direct3D 11 裝置和裝置內容物件。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-109">This section describes Direct3D 11 device and device-context objects.</span></span> |
| [<span data-ttu-id="0ffbe-110">資源</span><span class="sxs-lookup"><span data-stu-id="0ffbe-110">Resources</span></span>](overviews-direct3d-11-resources.md) | <span data-ttu-id="0ffbe-111">本節說明 Direct3D 11 資源的各個層面。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-111">This section describes aspects of Direct3D 11 resources.</span></span> |
| [<span data-ttu-id="0ffbe-112">圖形管線</span><span class="sxs-lookup"><span data-stu-id="0ffbe-112">Graphics pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md) | <span data-ttu-id="0ffbe-113">本節說明 Direct3D 11 可程式化管線。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-113">This section describes the Direct3D 11 programmable pipeline.</span></span> |
| [<span data-ttu-id="0ffbe-114">計算著色器總覽</span><span class="sxs-lookup"><span data-stu-id="0ffbe-114">Compute shader overview</span></span>](direct3d-11-advanced-stages-compute-shader.md) | <span data-ttu-id="0ffbe-115">計算著色器是可程式化的著色器階段，可將 Direct3D 11 擴充到圖形程式設計之外。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-115">A compute shader is a programmable shader stage that expands Direct3D 11 beyond graphics programming.</span></span> <span data-ttu-id="0ffbe-116">計算著色器技術也稱為 DirectCompute 技術。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-116">The compute shader technology is also known as the DirectCompute technology.</span></span> |
| [<span data-ttu-id="0ffbe-117">轉譯</span><span class="sxs-lookup"><span data-stu-id="0ffbe-117">Rendering</span></span>](overviews-direct3d-11-render.md) | <span data-ttu-id="0ffbe-118">本節包含數個 Direct3D 11 轉譯技術的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-118">This section contains information about several Direct3D 11 rendering technologies.</span></span> |
| [<span data-ttu-id="0ffbe-119">影響</span><span class="sxs-lookup"><span data-stu-id="0ffbe-119">Effects</span></span>](d3d11-graphics-programming-guide-effects.md) | <span data-ttu-id="0ffbe-120">DirectX 效果是管線狀態的集合，由以 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) 撰寫的運算式所設定，以及某些特定于效果架構的語法。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-120">A DirectX effect is a collection of pipeline state, set by expressions written in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) and some syntax that is specific to the effect framework.</span></span> |
| [<span data-ttu-id="0ffbe-121">遷移至 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0ffbe-121">Migrating to Direct3D 11</span></span>](d3d11-programming-guide-migrating.md) | <span data-ttu-id="0ffbe-122">本節提供從舊版 Direct3D 遷移至 Direct3D 11 的資訊。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-122">This section provides info for migrating to Direct3D 11 from an earlier version of Direct3D.</span></span> |
| [<span data-ttu-id="0ffbe-123">Direct3D video 介面</span><span class="sxs-lookup"><span data-stu-id="0ffbe-123">Direct3D video interfaces</span></span>](direct3d-video-interfaces.md) | <span data-ttu-id="0ffbe-124">本主題列出 Direct3D 9Ex 中可用的 Direct3D video 介面，以及 windows 7 和更新版本的 windows 用戶端作業系統以及 Windows Server 2008 R2 和更新版本的 Windows server 作業系統支援的功能。</span><span class="sxs-lookup"><span data-stu-id="0ffbe-124">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="0ffbe-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ffbe-125">Related topics</span></span>

* [<span data-ttu-id="0ffbe-126">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="0ffbe-126">Direct3D 11 Graphics</span></span>](atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="0ffbe-127">圖形參考</span><span class="sxs-lookup"><span data-stu-id="0ffbe-127">Graphics Reference</span></span>](atoc-d3d11-graphics-reference.md)