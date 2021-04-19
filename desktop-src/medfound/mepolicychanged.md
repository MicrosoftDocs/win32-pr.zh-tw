---
description: 當資料流程的輸出原則變更時，由管線元件引發。 此事件僅適用于受保護的內容。
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: 'MEPolicyChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974589"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="6a618-104">MEPolicyChanged 事件</span><span class="sxs-lookup"><span data-stu-id="6a618-104">MEPolicyChanged event</span></span>

<span data-ttu-id="6a618-105">當資料流程的輸出原則變更時，由管線元件引發。</span><span class="sxs-lookup"><span data-stu-id="6a618-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="6a618-106">此事件僅適用于受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="6a618-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="6a618-107">事件值</span><span class="sxs-lookup"><span data-stu-id="6a618-107">Event values</span></span>

<span data-ttu-id="6a618-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="6a618-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6a618-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6a618-109">VARTYPE</span></span>                | <span data-ttu-id="6a618-110">Description</span><span class="sxs-lookup"><span data-stu-id="6a618-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a618-111">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="6a618-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="6a618-112">資料流程之新原則的 [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6a618-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6a618-113">備註</span><span class="sxs-lookup"><span data-stu-id="6a618-113">Remarks</span></span>

<span data-ttu-id="6a618-114">所有信任的輸出都必須處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="6a618-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="6a618-115">媒體基礎轉換 (MFTs) 透過 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) 方法接收此事件。</span><span class="sxs-lookup"><span data-stu-id="6a618-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="6a618-116">媒體接收器會透過 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法收到此事件。</span><span class="sxs-lookup"><span data-stu-id="6a618-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="6a618-117">受信任的輸出必須套用新的原則，或傳回不受支援的錯誤碼 MF \_ E \_ 原則 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6a618-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a618-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a618-118">Requirements</span></span>



| <span data-ttu-id="6a618-119">需求</span><span class="sxs-lookup"><span data-stu-id="6a618-119">Requirement</span></span> | <span data-ttu-id="6a618-120">值</span><span class="sxs-lookup"><span data-stu-id="6a618-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a618-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a618-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a618-122">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a618-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="6a618-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a618-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a618-124">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a618-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="6a618-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6a618-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a618-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="6a618-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a618-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a618-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a618-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="6a618-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




