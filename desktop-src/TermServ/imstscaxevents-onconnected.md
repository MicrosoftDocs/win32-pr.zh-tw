---
title: IMsTscAxEvents OnConnected 方法
description: 當用戶端控制項正在建立與遠端桌面工作階段主機 (RD 工作階段主機) server 的連接時呼叫。
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- OnConnected 方法遠端桌面服務
- OnConnected 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnConnected 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685863"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="1b64b-106">IMsTscAxEvents：： OnConnected 方法</span><span class="sxs-lookup"><span data-stu-id="1b64b-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="1b64b-107">當用戶端控制項正在建立與遠端桌面工作階段主機 (RD 工作階段主機) server 的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="1b64b-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b64b-108">語法</span><span class="sxs-lookup"><span data-stu-id="1b64b-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="1b64b-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b64b-109">Parameters</span></span>

<span data-ttu-id="1b64b-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1b64b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b64b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b64b-111">Return value</span></span>

<span data-ttu-id="1b64b-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1b64b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b64b-113">備註</span><span class="sxs-lookup"><span data-stu-id="1b64b-113">Remarks</span></span>

<span data-ttu-id="1b64b-114">在您的事件接收器中執行此方法，以接收控制項已建立與 RD 工作階段主機伺服器之連接的通知。</span><span class="sxs-lookup"><span data-stu-id="1b64b-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="1b64b-115">如需呼叫這個方法的詳細資訊，請參閱 [**IMsTscAxEvents：： OnLoginComplete**](imstscaxevents-onlogincomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1b64b-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="1b64b-116">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="1b64b-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b64b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b64b-117">Requirements</span></span>



| <span data-ttu-id="1b64b-118">需求</span><span class="sxs-lookup"><span data-stu-id="1b64b-118">Requirement</span></span> | <span data-ttu-id="1b64b-119">值</span><span class="sxs-lookup"><span data-stu-id="1b64b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b64b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b64b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b64b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b64b-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1b64b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b64b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b64b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b64b-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1b64b-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1b64b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b64b-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b64b-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b64b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1b64b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b64b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b64b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b64b-128">IID</span><span class="sxs-lookup"><span data-stu-id="1b64b-128">IID</span></span><br/>                      | <span data-ttu-id="1b64b-129">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="1b64b-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1b64b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b64b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b64b-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="1b64b-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





