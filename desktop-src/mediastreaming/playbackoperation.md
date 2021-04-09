---
title: PlaybackOperation 類別
description: 註冊事件處理常式，此處理程式會在其中一個 MediaRenderer 播放方法啟動的非同步作業完成時叫用，並提供方法來傳回作業的結果。
ms.assetid: 4899254A-C393-4D03-970F-CF272F4761B6
keywords:
- PlaybackOperation 類別媒體串流 API
- PlaybackOperation 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- PlaybackOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 796ef1765deb4226470df09395c8a2cd7670513f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678055"
---
# <a name="playbackoperation-class"></a><span data-ttu-id="97bd6-105">PlaybackOperation 類別</span><span class="sxs-lookup"><span data-stu-id="97bd6-105">PlaybackOperation class</span></span>

<span data-ttu-id="97bd6-106">註冊事件處理常式，此處理程式會在其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用，並提供方法來傳回作業的結果。</span><span class="sxs-lookup"><span data-stu-id="97bd6-106">Registers an event handler that is invoked when an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="97bd6-107">**PlaybackOperation** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97bd6-107">**PlaybackOperation** has these types of members:</span></span>

-   [<span data-ttu-id="97bd6-108">方法</span><span class="sxs-lookup"><span data-stu-id="97bd6-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="97bd6-109">屬性</span><span class="sxs-lookup"><span data-stu-id="97bd6-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="97bd6-110">方法</span><span class="sxs-lookup"><span data-stu-id="97bd6-110">Methods</span></span>

<span data-ttu-id="97bd6-111">**PlaybackOperation** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="97bd6-111">The **PlaybackOperation** class has these methods.</span></span>



| <span data-ttu-id="97bd6-112">方法</span><span class="sxs-lookup"><span data-stu-id="97bd6-112">Method</span></span>                                             | <span data-ttu-id="97bd6-113">描述</span><span class="sxs-lookup"><span data-stu-id="97bd6-113">Description</span></span>                                                                                                                                |
|:---------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97bd6-114">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="97bd6-114">**GetResults**</span></span>](playbackoperation-getresults.md) | <span data-ttu-id="97bd6-115">傳回由其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="97bd6-115">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="97bd6-116">屬性</span><span class="sxs-lookup"><span data-stu-id="97bd6-116">Properties</span></span>

<span data-ttu-id="97bd6-117">**PlaybackOperation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="97bd6-117">The **PlaybackOperation** class has these properties.</span></span>



| <span data-ttu-id="97bd6-118">屬性</span><span class="sxs-lookup"><span data-stu-id="97bd6-118">Property</span></span>                                                    | <span data-ttu-id="97bd6-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="97bd6-119">Access type</span></span>           | <span data-ttu-id="97bd6-120">Description</span><span class="sxs-lookup"><span data-stu-id="97bd6-120">Description</span></span>                                                                                                                                                                           |
|:------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97bd6-121">**Completed**</span><span class="sxs-lookup"><span data-stu-id="97bd6-121">**Completed**</span></span>](playbackoperation-completed.md)<br/> | <span data-ttu-id="97bd6-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="97bd6-122">Read/write</span></span><br/> | <span data-ttu-id="97bd6-123">取得或設定當其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="97bd6-123">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span> <br/> |



 

 

 





