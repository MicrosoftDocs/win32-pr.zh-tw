---
description: 傳送 TAPI 線路 \_ 要求訊息，以報告來自另一個應用程式的新要求抵達。
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: 'LINE_REQUEST 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989552"
---
# <a name="line_request-message"></a><span data-ttu-id="860f4-103">行 \_ 要求訊息</span><span class="sxs-lookup"><span data-stu-id="860f4-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="860f4-104">傳送 TAPI **線路 \_ 要求** 訊息，以報告來自另一個應用程式的新要求抵達。</span><span class="sxs-lookup"><span data-stu-id="860f4-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="860f4-105">參數</span><span class="sxs-lookup"><span data-stu-id="860f4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="860f4-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="860f4-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="860f4-107">未使用。</span><span class="sxs-lookup"><span data-stu-id="860f4-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="860f4-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="860f4-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="860f4-109">[**LineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)上所指定之應用程式的註冊實例。</span><span class="sxs-lookup"><span data-stu-id="860f4-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="860f4-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="860f4-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="860f4-111">新暫止要求的要求模式。</span><span class="sxs-lookup"><span data-stu-id="860f4-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="860f4-112">此參數會使用 [**LINEREQUESTMODE \_ 常數**](linerequestmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="860f4-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="860f4-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="860f4-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="860f4-114">此參數的條件為，如果 *dwParam1* 設為 LINEREQUESTMODE \_ DROP， *dwParam2* 就會包含要求 DROP 的應用程式 *hWnd* 。</span><span class="sxs-lookup"><span data-stu-id="860f4-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="860f4-115">否則，就不會使用 *dwParam2* 。</span><span class="sxs-lookup"><span data-stu-id="860f4-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="860f4-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="860f4-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="860f4-117">如果 *dwParam1* 設定為 LINEREQUESTMODE \_ DROP，則 *dwParam3* 的低序位字組會包含要求卸載之應用程式所指定的 *wRequestID* 。</span><span class="sxs-lookup"><span data-stu-id="860f4-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="860f4-118">否則，就不會使用 *dwParam3* 。</span><span class="sxs-lookup"><span data-stu-id="860f4-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="860f4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="860f4-119">Return value</span></span>

<span data-ttu-id="860f4-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="860f4-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="860f4-121">備註</span><span class="sxs-lookup"><span data-stu-id="860f4-121">Remarks</span></span>

<span data-ttu-id="860f4-122">**行 \_ 要求** 訊息會傳送至已針對對應的要求模式註冊的最高優先順序應用程式。</span><span class="sxs-lookup"><span data-stu-id="860f4-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="860f4-123">此訊息指出指定要求模式的輔助電話語音要求抵達。</span><span class="sxs-lookup"><span data-stu-id="860f4-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="860f4-124">如果 *dwParam1* 是 LINEREQUESTMODE \_ MAKECALL，應用程式可以使用對應的要求模式來叫用 [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) 來接收要求。</span><span class="sxs-lookup"><span data-stu-id="860f4-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="860f4-125">如果 *dwParam1* 是 LINEREQUESTMODE \_ DROP，則訊息會包含要求收件者執行要求所需的所有資料。</span><span class="sxs-lookup"><span data-stu-id="860f4-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="860f4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="860f4-126">Requirements</span></span>



| <span data-ttu-id="860f4-127">需求</span><span class="sxs-lookup"><span data-stu-id="860f4-127">Requirement</span></span> | <span data-ttu-id="860f4-128">值</span><span class="sxs-lookup"><span data-stu-id="860f4-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="860f4-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="860f4-129">TAPI version</span></span><br/> | <span data-ttu-id="860f4-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="860f4-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="860f4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="860f4-131">Header</span></span><br/>       | <dl> <span data-ttu-id="860f4-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="860f4-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860f4-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="860f4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860f4-134">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="860f4-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="860f4-135">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="860f4-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="860f4-136">**tapiRequestMakeCall**</span><span class="sxs-lookup"><span data-stu-id="860f4-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




