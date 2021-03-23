---
title: Direct Machine Learning (DirectML)
description: 直接機器學習 (DirectML) 是適用于機器學習的低層級 API。 它具有 DirectX 12 樣式的熟悉 (原生C++，nano-COM) 程式設計介面和工作流程。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103856"
---
# <a name="direct-machine-learning-directml"></a><span data-ttu-id="36e29-104">Direct Machine Learning (DirectML)</span><span class="sxs-lookup"><span data-stu-id="36e29-104">Direct Machine Learning (DirectML)</span></span>

<span data-ttu-id="36e29-105">直接機器學習 (DirectML) 是適用于機器學習的低層級 API。</span><span class="sxs-lookup"><span data-stu-id="36e29-105">Direct Machine Learning (DirectML) is a low-level API for machine learning.</span></span> <span data-ttu-id="36e29-106">它具有 DirectX 12 樣式的熟悉 (原生C++，nano-COM) 程式設計介面和工作流程。</span><span class="sxs-lookup"><span data-stu-id="36e29-106">It has a familiar (native C++, nano-COM) programming interface and workflow in the style of DirectX 12.</span></span> <span data-ttu-id="36e29-107">您可以將機器學習推斷工作負載整合到您的遊戲、引擎、中介軟體、後端或其他應用程式中。</span><span class="sxs-lookup"><span data-stu-id="36e29-107">You can integrate machine learning inferencing workloads into your game, engine, middleware, backend, or other application.</span></span> <span data-ttu-id="36e29-108">所有 DirectX 12 相容硬體都支援 DirectML。</span><span class="sxs-lookup"><span data-stu-id="36e29-108">DirectML is supported by all DirectX 12-compatible hardware.</span></span>

<span data-ttu-id="36e29-109">DirectML 是在 Windows 10 1903 版和對應版本的 Windows SDK 中引進。</span><span class="sxs-lookup"><span data-stu-id="36e29-109">DirectML is introduced in Windows 10, version 1903, and in the corresponding version of the Windows SDK.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="36e29-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="36e29-110">In this section</span></span>

| <span data-ttu-id="36e29-111">主題</span><span class="sxs-lookup"><span data-stu-id="36e29-111">Topic</span></span> | <span data-ttu-id="36e29-112">描述</span><span class="sxs-lookup"><span data-stu-id="36e29-112">Description</span></span> |
|-|-|
| [<span data-ttu-id="36e29-113">DirectML 簡介</span><span class="sxs-lookup"><span data-stu-id="36e29-113">Introduction to DirectML</span></span>](dml-intro.md) | <span data-ttu-id="36e29-114">直接機器學習 (DirectML) 是適用于機器學習 (ML) 的低層級 API。</span><span class="sxs-lookup"><span data-stu-id="36e29-114">Direct Machine Learning (DirectML) is a low-level API for machine learning (ML).</span></span> |
| [<span data-ttu-id="36e29-115">在 DirectML 中繫結</span><span class="sxs-lookup"><span data-stu-id="36e29-115">Binding in DirectML</span></span>](dml-binding.md) | <span data-ttu-id="36e29-116">在 DirectML 中 *，系* 結指的是在初始化和執行機器學習運算子期間，要用於 GPU 的管線附加資源。</span><span class="sxs-lookup"><span data-stu-id="36e29-116">In DirectML, *binding* refers to the attachment of resources to the pipeline for the GPU to use during the initialization and execution of your machine learning operators.</span></span> <span data-ttu-id="36e29-117">例如，這些資源可以是輸入和輸出張量，以及操作員需要的任何暫存或持續性資源。</span><span class="sxs-lookup"><span data-stu-id="36e29-117">These resources can be input and output tensors, for example, as well as any temporary or persistent resources that the operator needs.</span></span> |
| [<span data-ttu-id="36e29-118">DirectML 中的 UAV 障礙和資源狀態阻礙</span><span class="sxs-lookup"><span data-stu-id="36e29-118">UAV barriers and resource state barriers in DirectML</span></span>](dml-barriers.md) | <span data-ttu-id="36e29-119">描述阻礙的正確性優點，以及如何在 DirectML 中使用它們。</span><span class="sxs-lookup"><span data-stu-id="36e29-119">Describes the correctness benefits of barriers, and how you can work with them in DirectML.</span></span> |
| [<span data-ttu-id="36e29-120">使用進展來表示填補和記憶體版面配置</span><span class="sxs-lookup"><span data-stu-id="36e29-120">Using strides to express padding and memory layout</span></span>](dml-strides.md) | <span data-ttu-id="36e29-121">DirectML 張量是由稱為 *大小* 的屬性和 *tensor 的進展* 所描述。</span><span class="sxs-lookup"><span data-stu-id="36e29-121">DirectML tensors are described by properties known as the *sizes* and the *strides* of the tensor.</span></span> |
| [<span data-ttu-id="36e29-122">資源存留期和同步處理</span><span class="sxs-lookup"><span data-stu-id="36e29-122">Resource lifetime and synchronization</span></span>](dml-resource-lifetime.md) | <span data-ttu-id="36e29-123">為了避免未定義的行為，您的 DirectML 應用程式必須正確地管理 CPU 與 GPU 之間的物件存留期和同步處理。</span><span class="sxs-lookup"><span data-stu-id="36e29-123">In order to avoid undefined behavior, your DirectML application must correctly manage object lifetimes and synchronization between the CPU and the GPU.</span></span> |
| [<span data-ttu-id="36e29-124">使用 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="36e29-124">Using the DirectML debug layer</span></span>](dml-debug-layer.md) | <span data-ttu-id="36e29-125">DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="36e29-125">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> |
| [<span data-ttu-id="36e29-126">處理錯誤和裝置移除</span><span class="sxs-lookup"><span data-stu-id="36e29-126">Handling errors and device-removal</span></span>](dml-errors.md) | <span data-ttu-id="36e29-127">本主題討論如何將 DirectML 裝置移除和其他錯誤情況進行調試。</span><span class="sxs-lookup"><span data-stu-id="36e29-127">This topic discusses how to debug DirectML device-removal, and other error conditions.</span></span> |
| [<span data-ttu-id="36e29-128">DirectML helper 函式</span><span class="sxs-lookup"><span data-stu-id="36e29-128">DirectML helper functions</span></span>](dml-helper-functions.md) | <span data-ttu-id="36e29-129">基本 DirectML helper 函數的程式代碼清單。</span><span class="sxs-lookup"><span data-stu-id="36e29-129">Code listings of essential DirectML helper functions.</span></span> |
| [<span data-ttu-id="36e29-130">DirectML 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="36e29-130">DirectML sample applications</span></span>](dml-min-app.md) | <span data-ttu-id="36e29-131">DirectML 範例應用程式的連結，包括基本 DirectML 應用程式的範例。</span><span class="sxs-lookup"><span data-stu-id="36e29-131">Links to DirectML sample applications, including a sample of a minimal DirectML application.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="36e29-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="36e29-132">Related topics</span></span>

* [<span data-ttu-id="36e29-133">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="36e29-133">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)
