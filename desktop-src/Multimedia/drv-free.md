---
title: 'DRV_FREE 訊息 (Mmsystem .h) '
description: 通知驅動程式正在將它從記憶體中移除。 驅動程式應該釋放任何已配置的記憶體和其他系統資源。
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935075"
---
# <a name="drv_free-message"></a><span data-ttu-id="37154-105">WINSPOOL.DRV \_ 可用訊息</span><span class="sxs-lookup"><span data-stu-id="37154-105">DRV\_FREE message</span></span>

<span data-ttu-id="37154-106">通知驅動程式正在將它從記憶體中移除。</span><span class="sxs-lookup"><span data-stu-id="37154-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="37154-107">驅動程式應該釋放任何已配置的記憶體和其他系統資源。</span><span class="sxs-lookup"><span data-stu-id="37154-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="37154-108">參數</span><span class="sxs-lookup"><span data-stu-id="37154-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37154-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="37154-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="37154-110">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="37154-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37154-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="37154-111">Return Value</span></span>

<span data-ttu-id="37154-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="37154-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37154-113">備註</span><span class="sxs-lookup"><span data-stu-id="37154-113">Remarks</span></span>

<span data-ttu-id="37154-114">不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="37154-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="37154-115">**Winspool.drv \_ FREE** 訊息一律是設備磁碟機收到的最後一則訊息。</span><span class="sxs-lookup"><span data-stu-id="37154-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="37154-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="37154-116">Requirements</span></span>



| <span data-ttu-id="37154-117">需求</span><span class="sxs-lookup"><span data-stu-id="37154-117">Requirement</span></span> | <span data-ttu-id="37154-118">值</span><span class="sxs-lookup"><span data-stu-id="37154-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37154-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37154-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37154-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37154-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37154-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37154-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37154-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37154-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37154-123">標頭</span><span class="sxs-lookup"><span data-stu-id="37154-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37154-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="37154-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37154-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37154-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37154-126">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="37154-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="37154-127">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="37154-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





