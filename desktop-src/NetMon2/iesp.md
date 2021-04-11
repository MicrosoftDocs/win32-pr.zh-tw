---
description: IESP 介面提供將 NPP 連接到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及將 NPP 從網路中斷連線。
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: 'IESP 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112801"
---
# <a name="iesp-interface"></a><span data-ttu-id="dee9e-103">IESP 介面</span><span class="sxs-lookup"><span data-stu-id="dee9e-103">IESP interface</span></span>

<span data-ttu-id="dee9e-104">**IESP** 介面提供將 NPP 連接到網路的方法、捕捉至 capture 檔案的網路流量、取出統計資料，以及將 NPP 從網路中斷連線。</span><span class="sxs-lookup"><span data-stu-id="dee9e-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="dee9e-105">當您需要收集專屬 ESP 檔案格式的網路 [*對話統計資料*](c.md) 時，主要會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="dee9e-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="dee9e-106">成員</span><span class="sxs-lookup"><span data-stu-id="dee9e-106">Members</span></span>

<span data-ttu-id="dee9e-107">**IESP** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="dee9e-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dee9e-108">**IESP** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dee9e-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="dee9e-109">方法</span><span class="sxs-lookup"><span data-stu-id="dee9e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dee9e-110">方法</span><span class="sxs-lookup"><span data-stu-id="dee9e-110">Methods</span></span>

<span data-ttu-id="dee9e-111">**IESP** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dee9e-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="dee9e-112">方法</span><span class="sxs-lookup"><span data-stu-id="dee9e-112">Method</span></span>                                          | <span data-ttu-id="dee9e-113">描述</span><span class="sxs-lookup"><span data-stu-id="dee9e-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee9e-114">**設定**</span><span class="sxs-lookup"><span data-stu-id="dee9e-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="dee9e-115">提交 capture 的設定資訊</span><span class="sxs-lookup"><span data-stu-id="dee9e-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="dee9e-116">**連接**</span><span class="sxs-lookup"><span data-stu-id="dee9e-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="dee9e-117">將 NPP 連接到網路。</span><span class="sxs-lookup"><span data-stu-id="dee9e-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="dee9e-118">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="dee9e-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="dee9e-119">中斷 NPP 與網路的連線。</span><span class="sxs-lookup"><span data-stu-id="dee9e-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="dee9e-120">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="dee9e-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="dee9e-121">[*抓取 capture*](c.md)的狀態，指出 capture 正在執行或已暫停。</span><span class="sxs-lookup"><span data-stu-id="dee9e-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="dee9e-122">**暫停**</span><span class="sxs-lookup"><span data-stu-id="dee9e-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="dee9e-123">暫時停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="dee9e-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dee9e-124">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="dee9e-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="dee9e-125">抓取使用網路監視器在子網上捕獲資料的所有電腦清單。</span><span class="sxs-lookup"><span data-stu-id="dee9e-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="dee9e-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="dee9e-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="dee9e-127">抓取 NPP 的狀態。</span><span class="sxs-lookup"><span data-stu-id="dee9e-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="dee9e-128">**繼續**</span><span class="sxs-lookup"><span data-stu-id="dee9e-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="dee9e-129">繼續暫停的捕獲。</span><span class="sxs-lookup"><span data-stu-id="dee9e-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="dee9e-130">**開始**</span><span class="sxs-lookup"><span data-stu-id="dee9e-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="dee9e-131">啟動 capture 並建立檔案。</span><span class="sxs-lookup"><span data-stu-id="dee9e-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="dee9e-132">**停止**</span><span class="sxs-lookup"><span data-stu-id="dee9e-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="dee9e-133">停止目前的捕獲。</span><span class="sxs-lookup"><span data-stu-id="dee9e-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="dee9e-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="dee9e-134">Requirements</span></span>



| <span data-ttu-id="dee9e-135">需求</span><span class="sxs-lookup"><span data-stu-id="dee9e-135">Requirement</span></span> | <span data-ttu-id="dee9e-136">值</span><span class="sxs-lookup"><span data-stu-id="dee9e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee9e-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dee9e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dee9e-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee9e-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dee9e-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dee9e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dee9e-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee9e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dee9e-141">標頭</span><span class="sxs-lookup"><span data-stu-id="dee9e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee9e-142"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="dee9e-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dee9e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dee9e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee9e-144"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee9e-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

