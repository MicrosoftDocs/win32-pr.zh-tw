---
title: IMsTscAxEvents OnNetworkStatusChanged 方法
description: 在網路狀態變更時呼叫。 |IMsTscAxEvents OnNetworkStatusChanged 方法
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged 方法遠端桌面服務
- OnNetworkStatusChanged 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnNetworkStatusChanged 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979860"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="3b0e5-107">IMsTscAxEvents：： OnNetworkStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="3b0e5-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="3b0e5-108">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0e5-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b0e5-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="3b0e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b0e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b0e5-111">*qualityLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b0e5-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-112">指定新的連線速度。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-112">Specifies the new connection speed.</span></span> <span data-ttu-id="3b0e5-113">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="3b0e5-114">1</span><span class="sxs-lookup"><span data-stu-id="3b0e5-114">1</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-115">每秒小於 512 kb (KBps) 。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="3b0e5-116">2</span><span class="sxs-lookup"><span data-stu-id="3b0e5-116">2</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-117">512到 1999 KBps。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="3b0e5-118">3</span><span class="sxs-lookup"><span data-stu-id="3b0e5-118">3</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-119">2000到 9999 KBps。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="3b0e5-120">4</span><span class="sxs-lookup"><span data-stu-id="3b0e5-120">4</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-121">大於或等於 10000 KBps。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3b0e5-122">*頻寬* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b0e5-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-123">指定連接頻寬。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="3b0e5-124">*rtt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b0e5-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0e5-125">指定連接延遲。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b0e5-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b0e5-126">Return value</span></span>

<span data-ttu-id="3b0e5-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b0e5-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b0e5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b0e5-128">Requirements</span></span>



| <span data-ttu-id="3b0e5-129">需求</span><span class="sxs-lookup"><span data-stu-id="3b0e5-129">Requirement</span></span> | <span data-ttu-id="3b0e5-130">值</span><span class="sxs-lookup"><span data-stu-id="3b0e5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0e5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b0e5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0e5-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3b0e5-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="3b0e5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b0e5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0e5-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b0e5-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="3b0e5-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3b0e5-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b0e5-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b0e5-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b0e5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3b0e5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0e5-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b0e5-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b0e5-139">IID</span><span class="sxs-lookup"><span data-stu-id="3b0e5-139">IID</span></span><br/>                      | <span data-ttu-id="3b0e5-140">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="3b0e5-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3b0e5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b0e5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0e5-142">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="3b0e5-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





