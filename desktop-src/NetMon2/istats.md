---
description: IStats 介面提供您用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。 此介面會產生不含框架的統計資料。
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: 'IStats 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970228"
---
# <a name="istats-interface"></a><span data-ttu-id="2fcd7-104">IStats 介面</span><span class="sxs-lookup"><span data-stu-id="2fcd7-104">IStats interface</span></span>

<span data-ttu-id="2fcd7-105">**IStats** 介面提供您用來將 NPP 連接到網路、捕捉網路流量、取出統計資料，以及將 NPP 從網路中斷連線的方法。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="2fcd7-106">此介面會產生不含框架的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="2fcd7-107">成員</span><span class="sxs-lookup"><span data-stu-id="2fcd7-107">Members</span></span>

<span data-ttu-id="2fcd7-108">**IStats** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2fcd7-109">**IStats** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2fcd7-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="2fcd7-110">方法</span><span class="sxs-lookup"><span data-stu-id="2fcd7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2fcd7-111">方法</span><span class="sxs-lookup"><span data-stu-id="2fcd7-111">Methods</span></span>

<span data-ttu-id="2fcd7-112">**IStats** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="2fcd7-113">方法</span><span class="sxs-lookup"><span data-stu-id="2fcd7-113">Method</span></span>                                                                | <span data-ttu-id="2fcd7-114">描述</span><span class="sxs-lookup"><span data-stu-id="2fcd7-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fcd7-115">**設定**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="2fcd7-116">設定捕獲檔案的觸發程式、模式比對和緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="2fcd7-117">**連接**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="2fcd7-118">將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="2fcd7-119">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="2fcd7-120">中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="2fcd7-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="2fcd7-122">[*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="2fcd7-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="2fcd7-124">抓取目前 capture 的 [*會話*](s.md) 和 [*工作站資訊*](s.md) 。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="2fcd7-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="2fcd7-126">從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="2fcd7-127">**暫停**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="2fcd7-128">暫時停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="2fcd7-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="2fcd7-130">抓取使用網路監視器在子網上捕獲資料的所有電腦清單。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="2fcd7-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="2fcd7-132">抓取 NPP 的狀態。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="2fcd7-133">**繼續**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="2fcd7-134">重新開機已暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="2fcd7-135">**開始**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="2fcd7-136">開始捕獲。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="2fcd7-137">**停止**</span><span class="sxs-lookup"><span data-stu-id="2fcd7-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="2fcd7-138">停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="2fcd7-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="2fcd7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fcd7-139">Requirements</span></span>



| <span data-ttu-id="2fcd7-140">需求</span><span class="sxs-lookup"><span data-stu-id="2fcd7-140">Requirement</span></span> | <span data-ttu-id="2fcd7-141">值</span><span class="sxs-lookup"><span data-stu-id="2fcd7-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcd7-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fcd7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcd7-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fcd7-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2fcd7-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fcd7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcd7-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fcd7-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2fcd7-146">標頭</span><span class="sxs-lookup"><span data-stu-id="2fcd7-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fcd7-147"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd7-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2fcd7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcd7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcd7-149"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd7-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

