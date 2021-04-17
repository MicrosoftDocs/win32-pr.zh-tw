---
title: 'DRV_EXITSESSION 訊息 (Mmsystem .h) '
description: 通知驅動程式 Windows 正在準備退出。 驅動程式應該準備終止。
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- DRV_EXITSESSION message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466929"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="6db58-105">WINSPOOL.DRV \_ EXITSESSION 訊息</span><span class="sxs-lookup"><span data-stu-id="6db58-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="6db58-106">通知驅動程式 Windows 正在準備退出。</span><span class="sxs-lookup"><span data-stu-id="6db58-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="6db58-107">驅動程式應該準備終止。</span><span class="sxs-lookup"><span data-stu-id="6db58-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="6db58-108">參數</span><span class="sxs-lookup"><span data-stu-id="6db58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db58-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="6db58-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="6db58-110">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6db58-110">Identifier of the installable driver.</span></span> <span data-ttu-id="6db58-111">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6db58-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6db58-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="6db58-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="6db58-113">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6db58-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db58-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6db58-114">Return Value</span></span>

<span data-ttu-id="6db58-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6db58-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db58-116">備註</span><span class="sxs-lookup"><span data-stu-id="6db58-116">Remarks</span></span>

<span data-ttu-id="6db58-117">不會使用 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="6db58-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db58-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6db58-118">Requirements</span></span>



| <span data-ttu-id="6db58-119">需求</span><span class="sxs-lookup"><span data-stu-id="6db58-119">Requirement</span></span> | <span data-ttu-id="6db58-120">值</span><span class="sxs-lookup"><span data-stu-id="6db58-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db58-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6db58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6db58-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6db58-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6db58-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6db58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6db58-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6db58-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6db58-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6db58-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db58-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6db58-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db58-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6db58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db58-128">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="6db58-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="6db58-129">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="6db58-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





