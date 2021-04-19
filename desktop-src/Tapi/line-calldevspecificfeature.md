---
description: TSPI LINE \_ CALLDEVSPECIFICFEATURE 訊息會傳送至 LINEEVENT 回呼函式，以通知 TAPI 有關線路或位址上發生的裝置特定事件。
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: 'LINE_CALLDEVSPECIFICFEATURE 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000962"
---
# <a name="line_calldevspecificfeature-message"></a><span data-ttu-id="c62e4-103">行 \_ CALLDEVSPECIFICFEATURE 訊息</span><span class="sxs-lookup"><span data-stu-id="c62e4-103">LINE\_CALLDEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="c62e4-104">TSPI **LINE \_ CALLDEVSPECIFICFEATURE** 訊息會傳送至 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼函式，以通知 TAPI 有關線路或位址上發生的裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="c62e4-104">The TSPI **LINE\_CALLDEVSPECIFICFEATURE** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a line or address.</span></span> <span data-ttu-id="c62e4-105">訊息的意義，以及 *dwParam1* 到 *dwParam3* 參數的解讀是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="c62e4-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c62e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="c62e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62e4-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="c62e4-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-108">線路裝置的 TAPI 不透明物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="c62e4-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="c62e4-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="c62e4-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-110">呼叫裝置的 TAPI 不透明物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="c62e4-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="c62e4-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="c62e4-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-112">值行 \_ CALLDEVSPECIFICFEATURE。</span><span class="sxs-lookup"><span data-stu-id="c62e4-112">The value LINE\_CALLDEVSPECIFICFEATURE.</span></span>

</dd> <dt>

<span data-ttu-id="c62e4-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c62e4-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-114">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c62e4-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="c62e4-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c62e4-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-116">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c62e4-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="c62e4-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c62e4-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e4-118">特定裝置。</span><span class="sxs-lookup"><span data-stu-id="c62e4-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c62e4-119">備註</span><span class="sxs-lookup"><span data-stu-id="c62e4-119">Remarks</span></span>

<span data-ttu-id="c62e4-120">服務提供者會搭配 [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)函式使用 **LINE \_ CALLDEVSPECIFICFEATURE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c62e4-120">The **LINE\_CALLDEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) function.</span></span> <span data-ttu-id="c62e4-121">其意義是裝置特定的。</span><span class="sxs-lookup"><span data-stu-id="c62e4-121">Its meaning is device specific.</span></span>

<span data-ttu-id="c62e4-122">TAPI 會將 [**\_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) 訊息傳送至應用程式，以回應從服務提供者接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="c62e4-122">TAPI sends the [**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="c62e4-123">*HtLine* 和 *htCall* 參數會轉譯為適當的 *hCall* ，作為 TAPI 層級的 *hDevice* 參數。</span><span class="sxs-lookup"><span data-stu-id="c62e4-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="c62e4-124">*DwParam1*、 *dwParam2* 和 *dwParam3* 參數會透過未修改的傳遞。</span><span class="sxs-lookup"><span data-stu-id="c62e4-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="c62e4-125">在 TAPI 層級沒有直接對應的訊息，但這則訊息與行 DEVSPECIFICFEATURE 非常類似 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c62e4-125">There is no directly corresponding message at the TAPI level, although this message is very similar to LINE\_DEVSPECIFICFEATURE.</span></span> <span data-ttu-id="c62e4-126">在 TSPI 層級，裝置專屬的功能訊息會在這些報表事件的行和位址之間進行分割，以及在呼叫上進行報告事件。</span><span class="sxs-lookup"><span data-stu-id="c62e4-126">At the TSPI level, the device-specific feature messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="c62e4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c62e4-127">Requirements</span></span>



| <span data-ttu-id="c62e4-128">需求</span><span class="sxs-lookup"><span data-stu-id="c62e4-128">Requirement</span></span> | <span data-ttu-id="c62e4-129">值</span><span class="sxs-lookup"><span data-stu-id="c62e4-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c62e4-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c62e4-130">TAPI version</span></span><br/> | <span data-ttu-id="c62e4-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c62e4-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c62e4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c62e4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="c62e4-133"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c62e4-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62e4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c62e4-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c62e4-135">[**行 \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c62e4-135">[**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c62e4-136">**TSPI \_ lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="c62e4-136">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

