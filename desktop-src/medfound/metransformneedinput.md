---
description: 由非同步媒體基礎轉換 (MFT) 傳送，以要求新的輸入範例。
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: 'METransformNeedInput 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113689"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="cf1ba-103">METransformNeedInput 事件</span><span class="sxs-lookup"><span data-stu-id="cf1ba-103">METransformNeedInput event</span></span>

<span data-ttu-id="cf1ba-104">由非同步媒體基礎轉換 (MFT) 傳送，以要求新的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="cf1ba-105">事件值</span><span class="sxs-lookup"><span data-stu-id="cf1ba-105">Event values</span></span>

<span data-ttu-id="cf1ba-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cf1ba-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cf1ba-107">VARTYPE</span></span>              | <span data-ttu-id="cf1ba-108">Description</span><span class="sxs-lookup"><span data-stu-id="cf1ba-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="cf1ba-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="cf1ba-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cf1ba-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="cf1ba-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cf1ba-111">Attributes</span></span>

<span data-ttu-id="cf1ba-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="cf1ba-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cf1ba-113">Attribute</span></span>                                                                        | <span data-ttu-id="cf1ba-114">描述</span><span class="sxs-lookup"><span data-stu-id="cf1ba-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf1ba-115">MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="cf1ba-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="cf1ba-116">需要輸入資料之資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="cf1ba-117">*需要 ()*</span><span class="sxs-lookup"><span data-stu-id="cf1ba-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cf1ba-118">備註</span><span class="sxs-lookup"><span data-stu-id="cf1ba-118">Remarks</span></span>

<span data-ttu-id="cf1ba-119">非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="cf1ba-120">同步 MFTs 不會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="cf1ba-121">當 MFT 用戶端收到此事件時，它應該呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 來傳遞下一個範例。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="cf1ba-122">事件物件的 [ [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼](mf-event-mft-input-stream-id.md) ] 屬性會指定需要資料的輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="cf1ba-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1ba-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf1ba-123">Requirements</span></span>



| <span data-ttu-id="cf1ba-124">需求</span><span class="sxs-lookup"><span data-stu-id="cf1ba-124">Requirement</span></span> | <span data-ttu-id="cf1ba-125">值</span><span class="sxs-lookup"><span data-stu-id="cf1ba-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1ba-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf1ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1ba-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf1ba-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="cf1ba-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf1ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1ba-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf1ba-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="cf1ba-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cf1ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf1ba-131"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="cf1ba-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1ba-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf1ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1ba-133">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="cf1ba-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="cf1ba-134">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="cf1ba-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




