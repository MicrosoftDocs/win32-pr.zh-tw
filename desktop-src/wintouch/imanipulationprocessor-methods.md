---
title: '方法 (IInertiaProcessor) '
description: 本節包含 IInertiaProcessor 介面的方法。
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch，IInertiaProcessor 介面
- Windows Touch，介面方法
- 慣性、IInertiaProcessor 介面
- IInertiaProcessor 介面，方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967514"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="6dd44-107">方法 (IInertiaProcessor) </span><span class="sxs-lookup"><span data-stu-id="6dd44-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="6dd44-108">本節包含 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="6dd44-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="6dd44-109">方法</span><span class="sxs-lookup"><span data-stu-id="6dd44-109">Method</span></span>                                                 | <span data-ttu-id="6dd44-110">描述</span><span class="sxs-lookup"><span data-stu-id="6dd44-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dd44-111">**重設**</span><span class="sxs-lookup"><span data-stu-id="6dd44-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="6dd44-112">使用初始時間戳記初始化處理器，並重新啟動慣性。</span><span class="sxs-lookup"><span data-stu-id="6dd44-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="6dd44-113">**處理序**</span><span class="sxs-lookup"><span data-stu-id="6dd44-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="6dd44-114">針對目前的刻度執行計算，並根據外推是否已完成來引發 **差異** 或 **已完成** 的事件。</span><span class="sxs-lookup"><span data-stu-id="6dd44-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="6dd44-115">如果在上一個刻度完成推斷，則方法為無作業。</span><span class="sxs-lookup"><span data-stu-id="6dd44-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="6dd44-116">**ProcessTime**</span><span class="sxs-lookup"><span data-stu-id="6dd44-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="6dd44-117">針對指定的刻度執行計算，並根據外推是否已完成來引發 **Delta** 或 **Completed** 事件。</span><span class="sxs-lookup"><span data-stu-id="6dd44-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="6dd44-118">**完成**</span><span class="sxs-lookup"><span data-stu-id="6dd44-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="6dd44-119">完成目前的操作，並停止慣性處理器上的慣性。</span><span class="sxs-lookup"><span data-stu-id="6dd44-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="6dd44-120">**CompleteTime**</span><span class="sxs-lookup"><span data-stu-id="6dd44-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="6dd44-121">在指定的刻度完成目前的操作、停止慣性處理器上的慣性，並引發 System.windows.uielement.manipulationcompleted> 事件。</span><span class="sxs-lookup"><span data-stu-id="6dd44-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="6dd44-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6dd44-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd44-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="6dd44-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




