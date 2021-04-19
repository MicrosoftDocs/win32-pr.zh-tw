---
description: 當它無法接受來自上游解碼器的動態格式變更要求時，由 VMR-7 和 VMR-9 傳送。
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: 'EC_VMR_RECONNECTION_FAILED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994097"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="4df8a-103">EC \_ VMR 重新 \_ 連接 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="4df8a-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="4df8a-104">當它無法接受來自上游解碼器的動態格式變更要求時，由 VMR-7 和 VMR-9 傳送。</span><span class="sxs-lookup"><span data-stu-id="4df8a-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="4df8a-105">參數</span><span class="sxs-lookup"><span data-stu-id="4df8a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df8a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4df8a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4df8a-107"> (**HRESULT**) 從 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 傳回的狀態碼，而該 VMR 的輸入 pin 失敗了重新連接。</span><span class="sxs-lookup"><span data-stu-id="4df8a-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="4df8a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4df8a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4df8a-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="4df8a-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4df8a-110">備註</span><span class="sxs-lookup"><span data-stu-id="4df8a-110">Remarks</span></span>

<span data-ttu-id="4df8a-111">此事件會轉送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="4df8a-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df8a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4df8a-112">Requirements</span></span>



| <span data-ttu-id="4df8a-113">需求</span><span class="sxs-lookup"><span data-stu-id="4df8a-113">Requirement</span></span> | <span data-ttu-id="4df8a-114">值</span><span class="sxs-lookup"><span data-stu-id="4df8a-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4df8a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="4df8a-115">Header</span></span><br/> | <dl> <span data-ttu-id="4df8a-116"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="4df8a-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df8a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4df8a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df8a-118">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="4df8a-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4df8a-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="4df8a-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




