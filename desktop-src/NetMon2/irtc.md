---
description: IRTC 介面提供了用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: 'IRTC 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943880"
---
# <a name="irtc-interface"></a><span data-ttu-id="97249-103">IRTC 介面</span><span class="sxs-lookup"><span data-stu-id="97249-103">IRTC interface</span></span>

<span data-ttu-id="97249-104">**IRTC** 介面提供了用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。</span><span class="sxs-lookup"><span data-stu-id="97249-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="97249-105">**IRTC** 會取得僅限本機進入點的介面，這是參與即時捕捉的必要專案。</span><span class="sxs-lookup"><span data-stu-id="97249-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="97249-106">此介面包含可將回呼交給 NPP 的方法。</span><span class="sxs-lookup"><span data-stu-id="97249-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="97249-107">成員</span><span class="sxs-lookup"><span data-stu-id="97249-107">Members</span></span>

<span data-ttu-id="97249-108">**IRTC** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="97249-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97249-109">**IRTC** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97249-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="97249-110">方法</span><span class="sxs-lookup"><span data-stu-id="97249-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97249-111">方法</span><span class="sxs-lookup"><span data-stu-id="97249-111">Methods</span></span>

<span data-ttu-id="97249-112">**IRTC** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="97249-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="97249-113">方法</span><span class="sxs-lookup"><span data-stu-id="97249-113">Method</span></span>                                                              | <span data-ttu-id="97249-114">描述</span><span class="sxs-lookup"><span data-stu-id="97249-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97249-115">**設定**</span><span class="sxs-lookup"><span data-stu-id="97249-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="97249-116">設定捕捉的觸發程式、模式比對和緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="97249-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="97249-117">**連接**</span><span class="sxs-lookup"><span data-stu-id="97249-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="97249-118">將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="97249-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="97249-119">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="97249-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="97249-120">中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="97249-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="97249-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="97249-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="97249-122">[*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="97249-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="97249-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="97249-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="97249-124">抓取目前 capture 的 [*會話*](s.md) 和 [*站資訊*](s.md) 。</span><span class="sxs-lookup"><span data-stu-id="97249-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="97249-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="97249-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="97249-126">從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="97249-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="97249-127">**暫停**</span><span class="sxs-lookup"><span data-stu-id="97249-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="97249-128">暫時停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="97249-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="97249-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="97249-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="97249-130">抓取子網上使用網路監視器來捕捉網路資料的所有電腦清單。</span><span class="sxs-lookup"><span data-stu-id="97249-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="97249-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="97249-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="97249-132">抓取 NPP 的狀態。</span><span class="sxs-lookup"><span data-stu-id="97249-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="97249-133">**繼續**</span><span class="sxs-lookup"><span data-stu-id="97249-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="97249-134">重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="97249-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="97249-135">**開始**</span><span class="sxs-lookup"><span data-stu-id="97249-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="97249-136">開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="97249-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="97249-137">**停止**</span><span class="sxs-lookup"><span data-stu-id="97249-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="97249-138">停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="97249-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="97249-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="97249-139">Requirements</span></span>



| <span data-ttu-id="97249-140">需求</span><span class="sxs-lookup"><span data-stu-id="97249-140">Requirement</span></span> | <span data-ttu-id="97249-141">值</span><span class="sxs-lookup"><span data-stu-id="97249-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97249-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97249-142">Minimum supported client</span></span><br/> | <span data-ttu-id="97249-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97249-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="97249-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97249-144">Minimum supported server</span></span><br/> | <span data-ttu-id="97249-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97249-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="97249-146">標頭</span><span class="sxs-lookup"><span data-stu-id="97249-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="97249-147"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="97249-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="97249-148">DLL</span><span class="sxs-lookup"><span data-stu-id="97249-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97249-149"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97249-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

