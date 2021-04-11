---
description: 當其中一個輸出保護設定的設定變更時，由管線元件引發。 此事件僅適用于受保護的內容。
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: 'MEContentProtectionMessage 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691268"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="70c0f-104">MEContentProtectionMessage 事件</span><span class="sxs-lookup"><span data-stu-id="70c0f-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="70c0f-105">當其中一個輸出保護設定的設定變更時，由管線元件引發。</span><span class="sxs-lookup"><span data-stu-id="70c0f-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="70c0f-106">此事件僅適用于受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="70c0f-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="70c0f-107">事件值</span><span class="sxs-lookup"><span data-stu-id="70c0f-107">Event values</span></span>

<span data-ttu-id="70c0f-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="70c0f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="70c0f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="70c0f-109">VARTYPE</span></span>              | <span data-ttu-id="70c0f-110">Description</span><span class="sxs-lookup"><span data-stu-id="70c0f-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="70c0f-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="70c0f-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="70c0f-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="70c0f-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="70c0f-113">備註</span><span class="sxs-lookup"><span data-stu-id="70c0f-113">Remarks</span></span>

<span data-ttu-id="70c0f-114">所有信任的輸出都必須處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="70c0f-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="70c0f-115">媒體基礎轉換 (MFTs) 透過 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) 方法接收此事件。</span><span class="sxs-lookup"><span data-stu-id="70c0f-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="70c0f-116">媒體接收器會透過 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法收到此事件。</span><span class="sxs-lookup"><span data-stu-id="70c0f-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="70c0f-117">受信任的輸出必須套用原則變更，或傳回不支援的錯誤碼 MF \_ E \_ 原則 \_ 。</span><span class="sxs-lookup"><span data-stu-id="70c0f-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="70c0f-118">事件資料和屬性取決於使用中的內容保護系統。</span><span class="sxs-lookup"><span data-stu-id="70c0f-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c0f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="70c0f-119">Requirements</span></span>



| <span data-ttu-id="70c0f-120">需求</span><span class="sxs-lookup"><span data-stu-id="70c0f-120">Requirement</span></span> | <span data-ttu-id="70c0f-121">值</span><span class="sxs-lookup"><span data-stu-id="70c0f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c0f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70c0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70c0f-123">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70c0f-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="70c0f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70c0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70c0f-125">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70c0f-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="70c0f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="70c0f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c0f-127"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="70c0f-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c0f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70c0f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c0f-129">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="70c0f-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




