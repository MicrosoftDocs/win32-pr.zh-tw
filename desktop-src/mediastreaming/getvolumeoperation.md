---
title: GetVolumeOperation 類別
description: 註冊當 GetVolumeAsync 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。
ms.assetid: F7BCE2AB-89B5-44CE-8BDF-347F2E3FD6C9
keywords:
- GetVolumeOperation 類別媒體串流 API
- GetVolumeOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- GetVolumeOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac06bfb85e8ebbf10306da43cb44c7e3b3e862a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966454"
---
# <a name="getvolumeoperation-class"></a><span data-ttu-id="86d54-105">GetVolumeOperation 類別</span><span class="sxs-lookup"><span data-stu-id="86d54-105">GetVolumeOperation class</span></span>

<span data-ttu-id="86d54-106">註冊當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。</span><span class="sxs-lookup"><span data-stu-id="86d54-106">Registers an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="86d54-107">**GetVolumeOperation** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86d54-107">**GetVolumeOperation** has these types of members:</span></span>

-   [<span data-ttu-id="86d54-108">方法</span><span class="sxs-lookup"><span data-stu-id="86d54-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="86d54-109">屬性</span><span class="sxs-lookup"><span data-stu-id="86d54-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86d54-110">方法</span><span class="sxs-lookup"><span data-stu-id="86d54-110">Methods</span></span>

<span data-ttu-id="86d54-111">**GetVolumeOperation** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86d54-111">The **GetVolumeOperation** class has these methods.</span></span>



| <span data-ttu-id="86d54-112">方法</span><span class="sxs-lookup"><span data-stu-id="86d54-112">Method</span></span>                                              | <span data-ttu-id="86d54-113">描述</span><span class="sxs-lookup"><span data-stu-id="86d54-113">Description</span></span>                                                                                                                      |
|:----------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86d54-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="86d54-114">**GetResults**</span></span>](getvolumeoperation-getresults.md) | <span data-ttu-id="86d54-115">傳回 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="86d54-115">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86d54-116">屬性</span><span class="sxs-lookup"><span data-stu-id="86d54-116">Properties</span></span>

<span data-ttu-id="86d54-117">**GetVolumeOperation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86d54-117">The **GetVolumeOperation** class has these properties.</span></span>



| <span data-ttu-id="86d54-118">屬性</span><span class="sxs-lookup"><span data-stu-id="86d54-118">Property</span></span>                                                     | <span data-ttu-id="86d54-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="86d54-119">Access type</span></span>           | <span data-ttu-id="86d54-120">Description</span><span class="sxs-lookup"><span data-stu-id="86d54-120">Description</span></span>                                                                                                                                                                |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86d54-121">**Completed**</span><span class="sxs-lookup"><span data-stu-id="86d54-121">**Completed**</span></span>](getvolumeoperation-completed.md)<br/> | <span data-ttu-id="86d54-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86d54-122">Read/write</span></span><br/> | <span data-ttu-id="86d54-123">取得或設定當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="86d54-123">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span> <br/> |



 

 

