---
title: 'DRV_ENABLE 訊息 (Mmsystem .h) '
description: 啟用驅動程式。 驅動程式應該初始化任何變數，並找出具有輸入和輸出 (i/o) 介面的裝置。
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935078"
---
# <a name="drv_enable-message"></a><span data-ttu-id="b8d70-105">WINSPOOL.DRV \_ 啟用訊息</span><span class="sxs-lookup"><span data-stu-id="b8d70-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="b8d70-106">啟用驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b8d70-106">Enables the driver.</span></span> <span data-ttu-id="b8d70-107">驅動程式應該初始化任何變數，並找出具有輸入和輸出 (i/o) 介面的裝置。</span><span class="sxs-lookup"><span data-stu-id="b8d70-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8d70-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8d70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d70-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="b8d70-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="b8d70-110">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8d70-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8d70-111">Return Value</span></span>

<span data-ttu-id="b8d70-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8d70-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d70-113">備註</span><span class="sxs-lookup"><span data-stu-id="b8d70-113">Remarks</span></span>

<span data-ttu-id="b8d70-114">不會使用 *dwDriverId*、 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="b8d70-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="b8d70-115">驅動程式會在收到此訊息時視為已啟用，直到使用 [**Winspool.drv \_ 停**](drv-disable.md) 用訊息停用為止。</span><span class="sxs-lookup"><span data-stu-id="b8d70-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d70-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8d70-116">Requirements</span></span>



| <span data-ttu-id="b8d70-117">需求</span><span class="sxs-lookup"><span data-stu-id="b8d70-117">Requirement</span></span> | <span data-ttu-id="b8d70-118">值</span><span class="sxs-lookup"><span data-stu-id="b8d70-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d70-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8d70-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d70-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8d70-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8d70-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8d70-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d70-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8d70-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8d70-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b8d70-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8d70-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b8d70-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d70-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8d70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d70-126">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="b8d70-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="b8d70-127">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="b8d70-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





