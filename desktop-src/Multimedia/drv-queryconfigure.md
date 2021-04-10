---
title: 'DRV_QUERYCONFIGURE 訊息 (Mmsystem .h) '
description: 指示驅動程式指定它是否支援自訂設定。
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187307"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="8d8a1-104">WINSPOOL.DRV \_ QUERYCONFIGURE 訊息</span><span class="sxs-lookup"><span data-stu-id="8d8a1-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="8d8a1-105">指示驅動程式指定它是否支援自訂設定。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d8a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d8a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8a1-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="8d8a1-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="8d8a1-108">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-108">Identifier of the installable driver.</span></span> <span data-ttu-id="8d8a1-109">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="8d8a1-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="8d8a1-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="8d8a1-111">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8a1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d8a1-112">Return Value</span></span>

<span data-ttu-id="8d8a1-113">如果驅動程式可以顯示設定對話方塊，則傳回非零值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8a1-114">備註</span><span class="sxs-lookup"><span data-stu-id="8d8a1-114">Remarks</span></span>

<span data-ttu-id="8d8a1-115">不會使用 *lParam1* 和 *lParam2* 參數。</span><span class="sxs-lookup"><span data-stu-id="8d8a1-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8a1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d8a1-116">Requirements</span></span>



| <span data-ttu-id="8d8a1-117">需求</span><span class="sxs-lookup"><span data-stu-id="8d8a1-117">Requirement</span></span> | <span data-ttu-id="8d8a1-118">值</span><span class="sxs-lookup"><span data-stu-id="8d8a1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8a1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d8a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8a1-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8a1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8d8a1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d8a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8a1-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8a1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8d8a1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8d8a1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8a1-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8d8a1-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8a1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d8a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8a1-126">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="8d8a1-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="8d8a1-127">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="8d8a1-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





