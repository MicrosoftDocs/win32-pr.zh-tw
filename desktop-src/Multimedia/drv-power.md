---
title: 'DRV_POWER 訊息 (Mmsystem .h) '
description: 通知驅動程式開啟或關閉裝置電源。
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- DRV_POWER message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935071"
---
# <a name="drv_power-message"></a><span data-ttu-id="feb44-104">WINSPOOL.DRV \_ 電源訊息</span><span class="sxs-lookup"><span data-stu-id="feb44-104">DRV\_POWER message</span></span>

<span data-ttu-id="feb44-105">通知驅動程式開啟或關閉裝置電源。</span><span class="sxs-lookup"><span data-stu-id="feb44-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="feb44-106">參數</span><span class="sxs-lookup"><span data-stu-id="feb44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb44-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="feb44-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="feb44-108">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="feb44-108">Identifier of the installable driver.</span></span> <span data-ttu-id="feb44-109">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="feb44-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="feb44-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="feb44-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="feb44-111">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="feb44-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb44-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="feb44-112">Return Value</span></span>

<span data-ttu-id="feb44-113">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="feb44-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb44-114">備註</span><span class="sxs-lookup"><span data-stu-id="feb44-114">Remarks</span></span>

<span data-ttu-id="feb44-115">不會使用 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="feb44-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb44-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="feb44-116">Requirements</span></span>



| <span data-ttu-id="feb44-117">需求</span><span class="sxs-lookup"><span data-stu-id="feb44-117">Requirement</span></span> | <span data-ttu-id="feb44-118">值</span><span class="sxs-lookup"><span data-stu-id="feb44-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb44-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="feb44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="feb44-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="feb44-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="feb44-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="feb44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="feb44-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="feb44-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="feb44-123">標頭</span><span class="sxs-lookup"><span data-stu-id="feb44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb44-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="feb44-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb44-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feb44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb44-126">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="feb44-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="feb44-127">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="feb44-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





