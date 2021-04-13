---
title: 互動內容結構
description: 本節中的主題提供互動內容結構的參考規格。
ms.assetid: 38C5CE85-405B-455F-809D-19C77B8A217B
keywords:
- 使用者互動
- input
- 指標
- 觸控
- 滑鼠
- 手寫筆
- 手寫筆
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 975b1342c681d4d154ba31d31348e13063c9fc88
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/07/2020
ms.locfileid: "104374242"
---
# <a name="interaction-context-structures"></a><span data-ttu-id="90054-110">互動內容結構</span><span class="sxs-lookup"><span data-stu-id="90054-110">Interaction Context Structures</span></span>

<span data-ttu-id="90054-111">本節中的主題提供 [互動內容](interaction-context-portal.md) 結構的參考規格。</span><span class="sxs-lookup"><span data-stu-id="90054-111">The topics in this section provide the reference specifications for [Interaction Context](interaction-context-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="90054-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="90054-112">In this section</span></span>

| <span data-ttu-id="90054-113">主題</span><span class="sxs-lookup"><span data-stu-id="90054-113">Topic</span></span> | <span data-ttu-id="90054-114">描述</span><span class="sxs-lookup"><span data-stu-id="90054-114">Description</span></span> |
|---|---|
| [<span data-ttu-id="90054-115">**跨 \_ 幻燈片 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="90054-115">**CROSS\_SLIDE\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-cross_slide_parameter)<br/>                           | <span data-ttu-id="90054-116">定義交叉投影片閾值和其距離閾值。</span><span class="sxs-lookup"><span data-stu-id="90054-116">Defines the cross-slide threshold and its distance threshold.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="90054-117">**互動 \_ 引數 \_ 交叉投影 \_ 片**</span><span class="sxs-lookup"><span data-stu-id="90054-117">**INTERACTION\_ARGUMENTS\_CROSS\_SLIDE**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide)<br/>  | <span data-ttu-id="90054-118">定義跨幻燈片互動的狀態。</span><span class="sxs-lookup"><span data-stu-id="90054-118">Defines the state of the cross-slide interaction.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="90054-119">**互動 \_ 引數 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="90054-119">**INTERACTION\_ARGUMENTS\_MANIPULATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation)<br/> | <span data-ttu-id="90054-120">定義操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="90054-120">Defines the state of a manipulation.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="90054-121">**互動 \_ 引數點 \_ 路**</span><span class="sxs-lookup"><span data-stu-id="90054-121">**INTERACTION\_ARGUMENTS\_TAP**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_tap)<br/>                   | <span data-ttu-id="90054-122">定義點路互動的狀態。</span><span class="sxs-lookup"><span data-stu-id="90054-122">Defines the state of the tap interaction.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="90054-123">**互動 \_ 內容 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="90054-123">**INTERACTION\_CONTEXT\_CONFIGURATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_configuration)<br/>   | <span data-ttu-id="90054-124">定義 [互動內容](interaction-context-portal.md) 物件的設定，以啟用、停用或修改互動的行為。</span><span class="sxs-lookup"><span data-stu-id="90054-124">Defines the configuration of an [Interaction Context](interaction-context-portal.md) object that enables, disables, or modifies the behavior of an interaction.</span></span><br/> |
| [<span data-ttu-id="90054-125">**互動 \_ 內容 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="90054-125">**INTERACTION\_CONTEXT\_OUTPUT**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_output)<br/>                 | <span data-ttu-id="90054-126">定義 [互動內容](interaction-context-portal.md) 物件的輸出。</span><span class="sxs-lookup"><span data-stu-id="90054-126">Defines the output of the [Interaction Context](interaction-context-portal.md) object.</span></span><br/>                                                                          |
| [<span data-ttu-id="90054-127">**操作 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="90054-127">**MANIPULATION\_TRANSFORM**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_transform)<br/>                          | <span data-ttu-id="90054-128">定義操作的轉換資料。</span><span class="sxs-lookup"><span data-stu-id="90054-128">Defines the transformation data for a manipulation.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="90054-129">**操作 \_ 速度**</span><span class="sxs-lookup"><span data-stu-id="90054-129">**MANIPULATION\_VELOCITY**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_velocity)<br/>                            | <span data-ttu-id="90054-130">定義操作的速度資料。</span><span class="sxs-lookup"><span data-stu-id="90054-130">Defines the velocity data of a manipulation.</span></span><br/>                                                                                                                     |
## <a name="related-topics"></a><span data-ttu-id="90054-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="90054-131">Related topics</span></span>

[<span data-ttu-id="90054-132">使用者互動</span><span class="sxs-lookup"><span data-stu-id="90054-132">User Interaction</span></span>](../user-interaction.md)
