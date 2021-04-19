---
title: IMsTscAxEvents OnAutoReconnecting2 方法
description: 當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。 |IMsTscAxEvents OnAutoReconnecting2 方法
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting2 方法遠端桌面服務
- OnAutoReconnecting2 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnecting2 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993834"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="be745-107">IMsTscAxEvents：： OnAutoReconnecting2 方法</span><span class="sxs-lookup"><span data-stu-id="be745-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="be745-108">當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="be745-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="be745-109">這是 [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) 方法的增強版本。</span><span class="sxs-lookup"><span data-stu-id="be745-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be745-110">語法</span><span class="sxs-lookup"><span data-stu-id="be745-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="be745-111">參數</span><span class="sxs-lookup"><span data-stu-id="be745-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be745-112">*disconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be745-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be745-113">描述上次會話中斷連接原因的程式碼。</span><span class="sxs-lookup"><span data-stu-id="be745-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="be745-114">*networkAvailable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be745-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be745-115">指定網路是否可用。</span><span class="sxs-lookup"><span data-stu-id="be745-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="be745-116">*了 attemptcount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be745-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be745-117">目前自動重新連接程式中所做的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="be745-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="be745-118">每次嘗試時，此計數都會增加一個。</span><span class="sxs-lookup"><span data-stu-id="be745-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="be745-119">*maxAttemptCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be745-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be745-120">目前自動重新連線程式中將會進行的嘗試次數上限。</span><span class="sxs-lookup"><span data-stu-id="be745-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be745-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="be745-121">Return value</span></span>

<span data-ttu-id="be745-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="be745-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be745-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="be745-123">Requirements</span></span>



| <span data-ttu-id="be745-124">需求</span><span class="sxs-lookup"><span data-stu-id="be745-124">Requirement</span></span> | <span data-ttu-id="be745-125">值</span><span class="sxs-lookup"><span data-stu-id="be745-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be745-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be745-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be745-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="be745-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="be745-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be745-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be745-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be745-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="be745-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="be745-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="be745-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be745-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="be745-132">DLL</span><span class="sxs-lookup"><span data-stu-id="be745-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be745-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be745-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be745-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be745-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be745-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="be745-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





