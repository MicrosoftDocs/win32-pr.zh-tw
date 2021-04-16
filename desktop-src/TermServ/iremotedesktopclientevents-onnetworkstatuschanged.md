---
title: IRemoteDesktopClientEvents OnNetworkStatusChanged 方法
description: 在網路狀態變更時呼叫。 |IRemoteDesktopClientEvents OnNetworkStatusChanged 方法
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged 方法遠端桌面服務
- OnNetworkStatusChanged 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnNetworkStatusChanged 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514433"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="e7a58-107">IRemoteDesktopClientEvents：： OnNetworkStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="e7a58-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="e7a58-108">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="e7a58-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a58-109">語法</span><span class="sxs-lookup"><span data-stu-id="e7a58-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="e7a58-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7a58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a58-111">*qualityLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7a58-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a58-112">連接的新品質層級。</span><span class="sxs-lookup"><span data-stu-id="e7a58-112">The new quality level of the connection.</span></span> <span data-ttu-id="e7a58-113">品質層級取決於頻寬和來回行程時間 (rtt) 值。</span><span class="sxs-lookup"><span data-stu-id="e7a58-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="e7a58-114">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e7a58-114">One of the following values.</span></span>



| <span data-ttu-id="e7a58-115">值</span><span class="sxs-lookup"><span data-stu-id="e7a58-115">Value</span></span>                                                                        | <span data-ttu-id="e7a58-116">意義</span><span class="sxs-lookup"><span data-stu-id="e7a58-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="e7a58-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e7a58-118">無法判斷品質層級。</span><span class="sxs-lookup"><span data-stu-id="e7a58-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="e7a58-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e7a58-120">連接品質很差 (一個橫條) 。</span><span class="sxs-lookup"><span data-stu-id="e7a58-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="e7a58-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e7a58-122">連接品質相當 (兩個橫條) 。</span><span class="sxs-lookup"><span data-stu-id="e7a58-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="e7a58-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e7a58-124">連接品質很適合 (三個橫條) 。</span><span class="sxs-lookup"><span data-stu-id="e7a58-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="e7a58-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="e7a58-126">連接品質很棒 (四個橫條) 。</span><span class="sxs-lookup"><span data-stu-id="e7a58-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e7a58-127">*頻寬* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7a58-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a58-128">指定新的連接頻寬，以 kb/秒為單位 (Kbps) 。</span><span class="sxs-lookup"><span data-stu-id="e7a58-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="e7a58-129">*rtt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7a58-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a58-130">指定新的連接往返時間 (延遲) （以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7a58-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7a58-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7a58-131">Return value</span></span>

<span data-ttu-id="e7a58-132">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e7a58-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a58-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7a58-133">Requirements</span></span>



| <span data-ttu-id="e7a58-134">需求</span><span class="sxs-lookup"><span data-stu-id="e7a58-134">Requirement</span></span> | <span data-ttu-id="e7a58-135">值</span><span class="sxs-lookup"><span data-stu-id="e7a58-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a58-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7a58-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a58-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7a58-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="e7a58-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7a58-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a58-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7a58-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="e7a58-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e7a58-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7a58-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e7a58-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a58-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a58-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a58-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e7a58-144">IID</span><span class="sxs-lookup"><span data-stu-id="e7a58-144">IID</span></span><br/>                      | <span data-ttu-id="e7a58-145">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="e7a58-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7a58-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7a58-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a58-147">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="e7a58-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





