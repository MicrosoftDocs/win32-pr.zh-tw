---
description: '\_系統會傳送 TAPI 線路 APPNEWCALL 訊息，以在有新的呼叫控制碼代表時通知應用程式。'
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: 'LINE_APPNEWCALL 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993589"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="93d78-103">行 \_ APPNEWCALL 訊息</span><span class="sxs-lookup"><span data-stu-id="93d78-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="93d78-104">系統會傳送 TAPI **線路 \_ APPNEWCALL** 訊息來通知應用程式，而不是透過應用程式中的 API 呼叫，以自發的方式 (建立新的呼叫控制碼，而在此情況下，會透過傳遞至函式) 的指標參數傳回控制碼。</span><span class="sxs-lookup"><span data-stu-id="93d78-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="93d78-105">參數</span><span class="sxs-lookup"><span data-stu-id="93d78-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d78-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="93d78-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="93d78-107">應用程式對已建立呼叫之線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="93d78-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="93d78-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="93d78-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="93d78-109">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="93d78-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="93d78-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="93d78-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="93d78-111">呼叫出現所在行的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="93d78-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="93d78-112">位址識別碼會永久與位址相關聯;識別碼在作業系統升級之間會維持不變。</span><span class="sxs-lookup"><span data-stu-id="93d78-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="93d78-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="93d78-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="93d78-114">應用程式對新呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="93d78-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="93d78-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="93d78-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="93d78-116">新呼叫 (LINECALLPRIVILEGE \_ 擁有者或 LINECALLPRIVILEGE 監視器) 的應用程式許可權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="93d78-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d78-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="93d78-117">Return value</span></span>

<span data-ttu-id="93d78-118">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="93d78-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d78-119">備註</span><span class="sxs-lookup"><span data-stu-id="93d78-119">Remarks</span></span>

<span data-ttu-id="93d78-120">只要應用程式有新呼叫的控制碼，就會傳送 **一行 \_ APPNEWCALL** 訊息給支援 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="93d78-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="93d78-121">由於訊息包含呼叫所在的 *hLine* 和 *dwAddressID* 參數，因此應用程式可以輕鬆地在正確的內容中建立新的呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="93d78-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="93d78-122">**行 \_ APPNEWCALL** 訊息一律緊接在 [**行 \_ CALLSTATE**](line-callstate.md)訊息中，指出呼叫的初始狀態。</span><span class="sxs-lookup"><span data-stu-id="93d78-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="93d78-123">協調早于 2.0) 之 API 版本的繼承應用程式 (只會傳送 [**\_ CALLSTATE**](line-callstate.md) 訊息，如舊版 api 中所述。</span><span class="sxs-lookup"><span data-stu-id="93d78-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="93d78-124">這類應用程式會在收到 [**一行 \_ CALLSTATE**](line-callstate.md) 訊息時建立新的呼叫物件，該訊息的 *dwParam3* 設定為非零值，並包含應用程式目前不知道的呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="93d78-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="93d78-125">缺點是 () 應用程式必須呼叫 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)來判斷與呼叫相關聯的 *hLine* 和 *dwAddressID* 參數; (b) 應用程式必須掃描所有已知的呼叫控制碼，以判斷呼叫是否為新的呼叫;而且 (c) 有可能，在某些情況下，應用程式會將它視為新的呼叫控制碼，但事實上，它只會將它的控制碼解除配置給呼叫 (例如，應用程式剛剛解除配置了呼叫控制碼，但因為另一個應用程式的 [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)已經在應用程式的 TAPI 訊息佇列中，所以提供呼叫應用程式擁有權的 [**行 \_ CALLSTATE**](line-callstate.md)訊息) 。</span><span class="sxs-lookup"><span data-stu-id="93d78-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="93d78-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="93d78-126">Requirements</span></span>



| <span data-ttu-id="93d78-127">需求</span><span class="sxs-lookup"><span data-stu-id="93d78-127">Requirement</span></span> | <span data-ttu-id="93d78-128">值</span><span class="sxs-lookup"><span data-stu-id="93d78-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93d78-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="93d78-129">TAPI version</span></span><br/> | <span data-ttu-id="93d78-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="93d78-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="93d78-131">標頭</span><span class="sxs-lookup"><span data-stu-id="93d78-131">Header</span></span><br/>       | <dl> <span data-ttu-id="93d78-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="93d78-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93d78-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93d78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d78-134">**行 \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="93d78-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="93d78-135">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="93d78-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="93d78-136">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="93d78-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




