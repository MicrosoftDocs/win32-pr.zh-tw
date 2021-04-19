---
title: IUniversalOrchestrator 介面
description: COM 介面，提供可讓用戶端與通用協調器進行通訊的方法。
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106992213"
---
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="923be-103">IUniversalOrchestrator 介面</span><span class="sxs-lookup"><span data-stu-id="923be-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="923be-104">此 API 屬於通用 Orchestrator API。</span><span class="sxs-lookup"><span data-stu-id="923be-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="923be-105">**IUniversalOrchestrator** 是提供下列方法的 COM 介面，可讓用戶端與通用協調器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="923be-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="923be-106">方法</span><span class="sxs-lookup"><span data-stu-id="923be-106">Methods</span></span>

|<span data-ttu-id="923be-107">方法</span><span class="sxs-lookup"><span data-stu-id="923be-107">Method</span></span> | <span data-ttu-id="923be-108">描述</span><span class="sxs-lookup"><span data-stu-id="923be-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="923be-109">::ScheduleWork</span><span class="sxs-lookup"><span data-stu-id="923be-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="923be-110">使用通用協調器註冊暫止的工作。</span><span class="sxs-lookup"><span data-stu-id="923be-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="923be-111">::WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="923be-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="923be-112">通知通用協調器所有工作都已完成。</span><span class="sxs-lookup"><span data-stu-id="923be-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="923be-113">::HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="923be-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="923be-114">查詢通用協調器，以判斷它是否會在新的裝置現成體驗之後立即運作。</span><span class="sxs-lookup"><span data-stu-id="923be-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="923be-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="923be-115">Requirements</span></span>

| <span data-ttu-id="923be-116">需求</span><span class="sxs-lookup"><span data-stu-id="923be-116">Requirement</span></span> | <span data-ttu-id="923be-117">版本</span><span class="sxs-lookup"><span data-stu-id="923be-117">Version</span></span> |
|---|---|
| <span data-ttu-id="923be-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="923be-118">Minimum supported client</span></span> | <span data-ttu-id="923be-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="923be-119">Windows 10 1903</span></span> |
|   |   |