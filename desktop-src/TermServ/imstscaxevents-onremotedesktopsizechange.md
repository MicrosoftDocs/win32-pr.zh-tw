---
title: IMsTscAxEvents OnRemoteDesktopSizeChange 方法
description: 呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- OnRemoteDesktopSizeChange 方法遠端桌面服務
- OnRemoteDesktopSizeChange 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteDesktopSizeChange 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508759"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="f3f5c-106">IMsTscAxEvents：： OnRemoteDesktopSizeChange 方法</span><span class="sxs-lookup"><span data-stu-id="f3f5c-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="f3f5c-107">呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f5c-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3f5c-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="f3f5c-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3f5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f5c-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3f5c-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f5c-111">已調整大小之遠端桌面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f3f5c-112">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3f5c-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f5c-113">已調整大小之遠端桌面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f5c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3f5c-114">Return value</span></span>

<span data-ttu-id="f3f5c-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f5c-116">備註</span><span class="sxs-lookup"><span data-stu-id="f3f5c-116">Remarks</span></span>

<span data-ttu-id="f3f5c-117">此事件可讓容器判斷它是否必須自行調整大小以回應用戶端控制作業，這可能會導致更大的可見桌面大小。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="f3f5c-118">請注意，此控制項將會自動調整新會話大小的捲軸。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="f3f5c-119">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f3f5c-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f5c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3f5c-120">Requirements</span></span>



| <span data-ttu-id="f3f5c-121">需求</span><span class="sxs-lookup"><span data-stu-id="f3f5c-121">Requirement</span></span> | <span data-ttu-id="f3f5c-122">值</span><span class="sxs-lookup"><span data-stu-id="f3f5c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f5c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3f5c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f5c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3f5c-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f3f5c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3f5c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f5c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3f5c-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f3f5c-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f3f5c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f3f5c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f5c-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3f5c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f5c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f5c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f5c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3f5c-131">IID</span><span class="sxs-lookup"><span data-stu-id="f3f5c-131">IID</span></span><br/>                      | <span data-ttu-id="f3f5c-132">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f3f5c-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f3f5c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3f5c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f5c-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





