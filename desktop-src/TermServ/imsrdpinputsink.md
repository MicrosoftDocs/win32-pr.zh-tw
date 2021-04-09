---
title: IMsRdpInputSink 介面
description: 遠端桌面輸入接收器。
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- IMsRdpInputSink 介面遠端桌面服務
- IMsRdpInputSink 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934124"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="5c990-105">IMsRdpInputSink 介面</span><span class="sxs-lookup"><span data-stu-id="5c990-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="5c990-106">遠端桌面輸入接收器。</span><span class="sxs-lookup"><span data-stu-id="5c990-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="5c990-107">成員</span><span class="sxs-lookup"><span data-stu-id="5c990-107">Members</span></span>

<span data-ttu-id="5c990-108">**IMsRdpInputSink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5c990-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5c990-109">**IMsRdpInputSink** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c990-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="5c990-110">方法</span><span class="sxs-lookup"><span data-stu-id="5c990-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c990-111">方法</span><span class="sxs-lookup"><span data-stu-id="5c990-111">Methods</span></span>

<span data-ttu-id="5c990-112">**IMsRdpInputSink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5c990-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="5c990-113">方法</span><span class="sxs-lookup"><span data-stu-id="5c990-113">Method</span></span>                                                               | <span data-ttu-id="5c990-114">描述</span><span class="sxs-lookup"><span data-stu-id="5c990-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="5c990-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="5c990-116">新增觸控輸入。</span><span class="sxs-lookup"><span data-stu-id="5c990-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="5c990-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="5c990-118">開始觸控框架。</span><span class="sxs-lookup"><span data-stu-id="5c990-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="5c990-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="5c990-120">結束觸控框架。</span><span class="sxs-lookup"><span data-stu-id="5c990-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="5c990-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="5c990-122">傳送鍵盤事件。</span><span class="sxs-lookup"><span data-stu-id="5c990-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="5c990-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="5c990-124">傳送滑鼠按鍵事件。</span><span class="sxs-lookup"><span data-stu-id="5c990-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="5c990-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="5c990-126">傳送滑鼠移動事件。</span><span class="sxs-lookup"><span data-stu-id="5c990-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="5c990-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="5c990-128">傳送滑鼠滾輪事件。</span><span class="sxs-lookup"><span data-stu-id="5c990-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="5c990-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c990-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="5c990-130">傳送同步處理事件。</span><span class="sxs-lookup"><span data-stu-id="5c990-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="5c990-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c990-131">Requirements</span></span>



| <span data-ttu-id="5c990-132">需求</span><span class="sxs-lookup"><span data-stu-id="5c990-132">Requirement</span></span> | <span data-ttu-id="5c990-133">值</span><span class="sxs-lookup"><span data-stu-id="5c990-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c990-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c990-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5c990-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5c990-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="5c990-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c990-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5c990-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5c990-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="5c990-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5c990-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c990-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c990-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c990-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5c990-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c990-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c990-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c990-142">IID</span><span class="sxs-lookup"><span data-stu-id="5c990-142">IID</span></span><br/>                      | <span data-ttu-id="5c990-143">IID \_ IMsRdpInputSink 定義為4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="5c990-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

