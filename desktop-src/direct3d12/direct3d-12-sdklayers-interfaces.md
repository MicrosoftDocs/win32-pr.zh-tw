---
title: Debug 圖層介面
description: 下列介面是在 d3d12sdklayers 中宣告。
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2020
ms.locfileid: "106967466"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="c25ef-103">Debug 圖層介面</span><span class="sxs-lookup"><span data-stu-id="c25ef-103">Debug Layer interfaces</span></span>

<span data-ttu-id="c25ef-104">下列介面是在中定義 `d3d12sdklayers.h` 。</span><span class="sxs-lookup"><span data-stu-id="c25ef-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c25ef-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="c25ef-105">In this section</span></span>

| <span data-ttu-id="c25ef-106">主題</span><span class="sxs-lookup"><span data-stu-id="c25ef-106">Topic</span></span> | <span data-ttu-id="c25ef-107">描述</span><span class="sxs-lookup"><span data-stu-id="c25ef-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="c25ef-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="c25ef-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="c25ef-109">Debug 介面會控制 debug 設定並驗證管線狀態。</span><span class="sxs-lookup"><span data-stu-id="c25ef-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="c25ef-110">只有在開啟 debug 層時，才能使用它。</span><span class="sxs-lookup"><span data-stu-id="c25ef-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="c25ef-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="c25ef-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="c25ef-112">將以 GPU 為基礎的驗證和相依的命令佇列同步處理新增至 debug 圖層。</span><span class="sxs-lookup"><span data-stu-id="c25ef-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="c25ef-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="c25ef-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="c25ef-114">加入可設定的 GPU-Based 驗證層級。</span><span class="sxs-lookup"><span data-stu-id="c25ef-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="c25ef-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="c25ef-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="c25ef-116">新增至 debug layer GPU 型驗證、相依的命令佇列同步處理，以及可設定的 GPU 型驗證層級。</span><span class="sxs-lookup"><span data-stu-id="c25ef-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="c25ef-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="c25ef-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="c25ef-118">提供監視和偵測命令清單的方法。</span><span class="sxs-lookup"><span data-stu-id="c25ef-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="c25ef-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="c25ef-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="c25ef-120">此介面可讓您修改其他命令清單的調試層設定。</span><span class="sxs-lookup"><span data-stu-id="c25ef-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="c25ef-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="c25ef-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="c25ef-122">提供監視和偵測命令佇列的方法。</span><span class="sxs-lookup"><span data-stu-id="c25ef-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="c25ef-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="c25ef-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="c25ef-124">此介面代表要進行偵錯工具的圖形裝置。</span><span class="sxs-lookup"><span data-stu-id="c25ef-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="c25ef-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="c25ef-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="c25ef-126">指定全裝置的調試層設定。</span><span class="sxs-lookup"><span data-stu-id="c25ef-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="c25ef-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="c25ef-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="c25ef-128">資訊佇列介面會儲存、抓取及篩選 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="c25ef-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="c25ef-129">佇列包含訊息佇列、選擇性的儲存體篩選堆疊，以及選擇性的抓取篩選堆疊。</span><span class="sxs-lookup"><span data-stu-id="c25ef-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="c25ef-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="c25ef-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="c25ef-131">D3D11On12 診斷層和圖形診斷工具之間的合約的一部分。</span><span class="sxs-lookup"><span data-stu-id="c25ef-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="c25ef-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c25ef-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c25ef-133">Direct3D 12 程式設計環境設定</span><span class="sxs-lookup"><span data-stu-id="c25ef-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="c25ef-134">Debug 圖層參考</span><span class="sxs-lookup"><span data-stu-id="c25ef-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="c25ef-135">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="c25ef-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>