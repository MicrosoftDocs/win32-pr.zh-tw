---
title: 'DRV_REMOVE 訊息 (Mmsystem .h) '
description: 通知驅動程式即將從系統中移除。 當驅動程式收到此訊息時，應移除它在登錄中建立的任何區段。
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025477"
---
# <a name="drv_remove-message"></a><span data-ttu-id="6094d-105">WINSPOOL.DRV \_ 移除訊息</span><span class="sxs-lookup"><span data-stu-id="6094d-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="6094d-106">通知驅動程式即將從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="6094d-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="6094d-107">當驅動程式收到此訊息時，應移除它在登錄中建立的任何區段。</span><span class="sxs-lookup"><span data-stu-id="6094d-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="6094d-108">參數</span><span class="sxs-lookup"><span data-stu-id="6094d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6094d-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="6094d-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="6094d-110">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6094d-110">Identifier of the installable driver.</span></span> <span data-ttu-id="6094d-111">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6094d-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6094d-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="6094d-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="6094d-113">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6094d-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6094d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6094d-114">Return Value</span></span>

<span data-ttu-id="6094d-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6094d-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6094d-116">備註</span><span class="sxs-lookup"><span data-stu-id="6094d-116">Remarks</span></span>

<span data-ttu-id="6094d-117">不會使用 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="6094d-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6094d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6094d-118">Requirements</span></span>



| <span data-ttu-id="6094d-119">需求</span><span class="sxs-lookup"><span data-stu-id="6094d-119">Requirement</span></span> | <span data-ttu-id="6094d-120">值</span><span class="sxs-lookup"><span data-stu-id="6094d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6094d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6094d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6094d-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6094d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6094d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6094d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6094d-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6094d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6094d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6094d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6094d-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6094d-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6094d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6094d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6094d-128">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="6094d-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="6094d-129">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="6094d-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





