---
title: Debug 圖層結構
description: 下列結構是在 d3d12sdklayers 中宣告。
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968061"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="25941-103">Debug 圖層結構</span><span class="sxs-lookup"><span data-stu-id="25941-103">Debug Layer Structures</span></span>

<span data-ttu-id="25941-104">下列結構是在 d3d12sdklayers 中宣告。</span><span class="sxs-lookup"><span data-stu-id="25941-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25941-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="25941-105">In this section</span></span>



| <span data-ttu-id="25941-106">主題</span><span class="sxs-lookup"><span data-stu-id="25941-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="25941-107">描述</span><span class="sxs-lookup"><span data-stu-id="25941-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25941-108">**D3D12 \_ DEBUG \_ 命令 \_ 清單以 \_ GPU 為基礎的 \_ \_ 驗證 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="25941-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="25941-109">描述 GPU-Based 驗證所使用的每個命令清單設定。</span><span class="sxs-lookup"><span data-stu-id="25941-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="25941-110">**D3D12 \_ DEBUG \_ 裝置 \_ GPU \_ 型 \_ 驗證 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="25941-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="25941-111">描述 GPU-Based 驗證所使用的設定。</span><span class="sxs-lookup"><span data-stu-id="25941-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="25941-112">**D3D12 \_ DEBUG \_ 裝置 \_ GPU \_ 緩慢 \_ 效能 \_ 因素**</span><span class="sxs-lookup"><span data-stu-id="25941-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="25941-113">描述由 debug 裝置插入以模擬較低效能圖形介面卡的人工速度。</span><span class="sxs-lookup"><span data-stu-id="25941-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="25941-114">**D3D12 \_ 資訊 \_ 佇列 \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="25941-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="25941-115">Debug 訊息篩選;包含要允許或拒絕的訊息類型清單。</span><span class="sxs-lookup"><span data-stu-id="25941-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="25941-116">**D3D12 \_ 資訊 \_ 佇列 \_ 篩選 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="25941-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="25941-117">允許或拒絕特定類型的訊息傳遞篩選。</span><span class="sxs-lookup"><span data-stu-id="25941-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="25941-118">**D3D12 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="25941-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="25941-119">資訊佇列中的 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="25941-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="25941-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="25941-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25941-121">Direct3D 12 程式設計環境設定</span><span class="sxs-lookup"><span data-stu-id="25941-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="25941-122">Debug 圖層參考</span><span class="sxs-lookup"><span data-stu-id="25941-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="25941-123">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="25941-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





