---
title: StreamSelectOperation 類別
description: 註冊當 GetMuteAsync 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。 |StreamSelectOperation 類別
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- StreamSelectOperation 類別媒體串流 API
- StreamSelectOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196031"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="17ff2-106">StreamSelectOperation 類別</span><span class="sxs-lookup"><span data-stu-id="17ff2-106">StreamSelectOperation class</span></span>

<span data-ttu-id="17ff2-107">註冊當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。</span><span class="sxs-lookup"><span data-stu-id="17ff2-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="17ff2-108">**StreamSelectOperation** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17ff2-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="17ff2-109">方法</span><span class="sxs-lookup"><span data-stu-id="17ff2-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="17ff2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="17ff2-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17ff2-111">方法</span><span class="sxs-lookup"><span data-stu-id="17ff2-111">Methods</span></span>

<span data-ttu-id="17ff2-112">**StreamSelectOperation** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="17ff2-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="17ff2-113">方法</span><span class="sxs-lookup"><span data-stu-id="17ff2-113">Method</span></span>                                                 | <span data-ttu-id="17ff2-114">描述</span><span class="sxs-lookup"><span data-stu-id="17ff2-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17ff2-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="17ff2-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="17ff2-116">傳回 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="17ff2-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="17ff2-117">屬性</span><span class="sxs-lookup"><span data-stu-id="17ff2-117">Properties</span></span>

<span data-ttu-id="17ff2-118">**StreamSelectOperation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17ff2-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="17ff2-119">屬性</span><span class="sxs-lookup"><span data-stu-id="17ff2-119">Property</span></span>                                                        | <span data-ttu-id="17ff2-120">存取類型</span><span class="sxs-lookup"><span data-stu-id="17ff2-120">Access type</span></span>           | <span data-ttu-id="17ff2-121">Description</span><span class="sxs-lookup"><span data-stu-id="17ff2-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17ff2-122">**Completed**</span><span class="sxs-lookup"><span data-stu-id="17ff2-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="17ff2-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17ff2-123">Read/write</span></span><br/> | <span data-ttu-id="17ff2-124">取得或設定當 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="17ff2-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

