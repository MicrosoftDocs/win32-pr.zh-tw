---
title: 'DRV_DISABLE 訊息 (Mmsystem .h) '
description: 停用驅動程式。 驅動程式應該將對應的裝置（如果有的話）置於非使用中狀態，並終止任何回呼函式或執行緒。
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935076"
---
# <a name="drv_disable-message"></a><span data-ttu-id="4abc5-105">WINSPOOL.DRV \_ 停用訊息</span><span class="sxs-lookup"><span data-stu-id="4abc5-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="4abc5-106">停用驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4abc5-106">Disables the driver.</span></span> <span data-ttu-id="4abc5-107">驅動程式應該將對應的裝置（如果有的話）置於非使用中狀態，並終止任何回呼函式或執行緒。</span><span class="sxs-lookup"><span data-stu-id="4abc5-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="4abc5-108">參數</span><span class="sxs-lookup"><span data-stu-id="4abc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abc5-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="4abc5-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="4abc5-110">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4abc5-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abc5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4abc5-111">Return Value</span></span>

<span data-ttu-id="4abc5-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4abc5-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4abc5-113">備註</span><span class="sxs-lookup"><span data-stu-id="4abc5-113">Remarks</span></span>

<span data-ttu-id="4abc5-114">不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="4abc5-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="4abc5-115">停用驅動程式之後，系統通常會在從記憶體移除驅動程式之前，先傳送 [**winspool.drv 的 \_ 可用**](drv-free.md) 訊息給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4abc5-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4abc5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4abc5-116">Requirements</span></span>



| <span data-ttu-id="4abc5-117">需求</span><span class="sxs-lookup"><span data-stu-id="4abc5-117">Requirement</span></span> | <span data-ttu-id="4abc5-118">值</span><span class="sxs-lookup"><span data-stu-id="4abc5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abc5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4abc5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4abc5-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4abc5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4abc5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4abc5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4abc5-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4abc5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4abc5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4abc5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4abc5-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4abc5-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abc5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4abc5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abc5-126">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="4abc5-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="4abc5-127">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="4abc5-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





