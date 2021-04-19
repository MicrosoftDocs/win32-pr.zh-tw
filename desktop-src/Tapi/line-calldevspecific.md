---
description: TSPI LINE \_ CALLDEVSPECIFIC 訊息會傳送至 LINEEVENT 回呼函式，以通知 TAPI 有關電話上發生的裝置特定事件。
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: 'LINE_CALLDEVSPECIFIC 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995937"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="0648c-103">行 \_ CALLDEVSPECIFIC 訊息</span><span class="sxs-lookup"><span data-stu-id="0648c-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="0648c-104">TSPI **LINE \_ CALLDEVSPECIFIC** 訊息會傳送至 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼函式，以通知 TAPI 有關電話上發生的裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="0648c-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="0648c-105">訊息的意義，以及 *dwParam1* 到 *dwParam3* 參數的解讀是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="0648c-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="0648c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0648c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0648c-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="0648c-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-108">線路裝置的 TAPI 不透明物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0648c-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="0648c-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="0648c-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-110">呼叫裝置的 TAPI 不透明物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0648c-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="0648c-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="0648c-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-112">值行 \_ CALLDEVSPECIFIC。</span><span class="sxs-lookup"><span data-stu-id="0648c-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="0648c-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0648c-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-114">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="0648c-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="0648c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0648c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-116">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="0648c-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="0648c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0648c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0648c-118">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="0648c-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0648c-119">備註</span><span class="sxs-lookup"><span data-stu-id="0648c-119">Remarks</span></span>

<span data-ttu-id="0648c-120">服務提供者會搭配 [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)函式使用 **LINE \_ CALLDEVSPECIFIC** 訊息。</span><span class="sxs-lookup"><span data-stu-id="0648c-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="0648c-121">其意義是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="0648c-121">Its meaning is device specific.</span></span>

<span data-ttu-id="0648c-122">TAPI 會將 [**\_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) 訊息傳送至應用程式，以回應從服務提供者接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="0648c-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="0648c-123">*HtLine* 和 *htCall* 參數會轉譯為適當的 *hCall* ，作為 TAPI 層級的 *hDevice* 參數。</span><span class="sxs-lookup"><span data-stu-id="0648c-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="0648c-124">*DwParam1*、 *dwParam2* 和 *dwParam3* 參數會透過未修改的傳遞。</span><span class="sxs-lookup"><span data-stu-id="0648c-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="0648c-125">在 TAPI 層級沒有直接對應的訊息，但這則訊息與 [**行 \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))非常類似。</span><span class="sxs-lookup"><span data-stu-id="0648c-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="0648c-126">在 TSPI 層級，裝置專屬的訊息會在這些報表事件的行和位址之間進行分割，以及在呼叫上進行報告事件。</span><span class="sxs-lookup"><span data-stu-id="0648c-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="0648c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0648c-127">Requirements</span></span>



| <span data-ttu-id="0648c-128">需求</span><span class="sxs-lookup"><span data-stu-id="0648c-128">Requirement</span></span> | <span data-ttu-id="0648c-129">值</span><span class="sxs-lookup"><span data-stu-id="0648c-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0648c-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0648c-130">TAPI version</span></span><br/> | <span data-ttu-id="0648c-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0648c-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0648c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0648c-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0648c-133"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0648c-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0648c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0648c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="0648c-135">[**行 \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0648c-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0648c-136">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="0648c-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="0648c-137">**TSPI \_ lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="0648c-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

