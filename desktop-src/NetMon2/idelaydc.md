---
description: IDelaydC 介面會提供用來連線到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及與網路中斷連線。
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: 'IDelaydC 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969225"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="724fe-103">IDelaydC 介面</span><span class="sxs-lookup"><span data-stu-id="724fe-103">IDelaydC interface</span></span>

<span data-ttu-id="724fe-104">**IDelaydC** 介面會提供用來連線到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及與網路中斷連線。</span><span class="sxs-lookup"><span data-stu-id="724fe-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="724fe-105">此介面會從網路資料流程捕獲框架，然後將畫面格複製到 capture 檔案。</span><span class="sxs-lookup"><span data-stu-id="724fe-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="724fe-106">網路監視器和 NPP 應用程式會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="724fe-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="724fe-107">若要接收網路資料，目標 NIC 必須支援混合模式。</span><span class="sxs-lookup"><span data-stu-id="724fe-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="724fe-108">成員</span><span class="sxs-lookup"><span data-stu-id="724fe-108">Members</span></span>

<span data-ttu-id="724fe-109">**IDelaydC** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="724fe-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="724fe-110">**IDelaydC** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="724fe-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="724fe-111">方法</span><span class="sxs-lookup"><span data-stu-id="724fe-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="724fe-112">方法</span><span class="sxs-lookup"><span data-stu-id="724fe-112">Methods</span></span>

<span data-ttu-id="724fe-113">**IDelaydC** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="724fe-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="724fe-114">方法</span><span class="sxs-lookup"><span data-stu-id="724fe-114">Method</span></span>                                                                  | <span data-ttu-id="724fe-115">描述</span><span class="sxs-lookup"><span data-stu-id="724fe-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="724fe-116">**設定**</span><span class="sxs-lookup"><span data-stu-id="724fe-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="724fe-117">提交用於捕捉的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="724fe-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="724fe-118">**連接**</span><span class="sxs-lookup"><span data-stu-id="724fe-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="724fe-119">將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="724fe-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="724fe-120">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="724fe-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="724fe-121">中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="724fe-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="724fe-122">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="724fe-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="724fe-123">[*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="724fe-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="724fe-124">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="724fe-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="724fe-125">抓取目前 capture 的 [*會話*](s.md) 和 [*站資訊*](s.md) 。</span><span class="sxs-lookup"><span data-stu-id="724fe-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="724fe-126">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="724fe-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="724fe-127">從目前執行中的 capture 解壓縮時間、緩衝區、驅動程式和其他網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="724fe-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="724fe-128">**暫停**</span><span class="sxs-lookup"><span data-stu-id="724fe-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="724fe-129">暫時停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="724fe-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="724fe-130">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="724fe-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="724fe-131">抓取使用網路監視器在子網上捕獲資料的所有電腦清單。</span><span class="sxs-lookup"><span data-stu-id="724fe-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="724fe-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="724fe-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="724fe-133">抓取 NPP 的狀態。</span><span class="sxs-lookup"><span data-stu-id="724fe-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="724fe-134">**繼續**</span><span class="sxs-lookup"><span data-stu-id="724fe-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="724fe-135">繼續暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="724fe-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="724fe-136">**開始**</span><span class="sxs-lookup"><span data-stu-id="724fe-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="724fe-137">啟動 [*capture 並建立檔案。*](c.md)</span><span class="sxs-lookup"><span data-stu-id="724fe-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="724fe-138">**停止**</span><span class="sxs-lookup"><span data-stu-id="724fe-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="724fe-139">停止目前的捕獲並關閉 [*capture*](c.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="724fe-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="724fe-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="724fe-140">Requirements</span></span>



| <span data-ttu-id="724fe-141">需求</span><span class="sxs-lookup"><span data-stu-id="724fe-141">Requirement</span></span> | <span data-ttu-id="724fe-142">值</span><span class="sxs-lookup"><span data-stu-id="724fe-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724fe-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="724fe-143">Minimum supported client</span></span><br/> | <span data-ttu-id="724fe-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="724fe-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="724fe-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="724fe-145">Minimum supported server</span></span><br/> | <span data-ttu-id="724fe-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="724fe-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="724fe-147">標頭</span><span class="sxs-lookup"><span data-stu-id="724fe-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="724fe-148"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="724fe-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="724fe-149">DLL</span><span class="sxs-lookup"><span data-stu-id="724fe-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="724fe-150"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="724fe-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

