---
title: 'DRV_LOAD 訊息 (Mmsystem .h) '
description: 通知驅動程式已載入它。 驅動程式應該確保任何需要的硬體和支援驅動程式都存在。
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935073"
---
# <a name="drv_load-message"></a><span data-ttu-id="50185-105">WINSPOOL.DRV \_ 載入訊息</span><span class="sxs-lookup"><span data-stu-id="50185-105">DRV\_LOAD message</span></span>

<span data-ttu-id="50185-106">通知驅動程式已載入它。</span><span class="sxs-lookup"><span data-stu-id="50185-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="50185-107">驅動程式應該確保任何需要的硬體和支援驅動程式都存在。</span><span class="sxs-lookup"><span data-stu-id="50185-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="50185-108">參數</span><span class="sxs-lookup"><span data-stu-id="50185-108">Parameters</span></span>

<span data-ttu-id="50185-109">*Hdrvr* 參數一律為零。</span><span class="sxs-lookup"><span data-stu-id="50185-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="50185-110">不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="50185-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="50185-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="50185-111">Return Value</span></span>

<span data-ttu-id="50185-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="50185-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="50185-113">備註</span><span class="sxs-lookup"><span data-stu-id="50185-113">Remarks</span></span>

<span data-ttu-id="50185-114">**Winspool.drv \_ 載入** 訊息一律是設備磁碟機所收到的第一則訊息。</span><span class="sxs-lookup"><span data-stu-id="50185-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="50185-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="50185-115">Requirements</span></span>



| <span data-ttu-id="50185-116">需求</span><span class="sxs-lookup"><span data-stu-id="50185-116">Requirement</span></span> | <span data-ttu-id="50185-117">值</span><span class="sxs-lookup"><span data-stu-id="50185-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50185-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50185-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50185-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50185-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="50185-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50185-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50185-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50185-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="50185-122">標頭</span><span class="sxs-lookup"><span data-stu-id="50185-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50185-123"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="50185-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50185-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50185-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50185-125">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="50185-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="50185-126">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="50185-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





