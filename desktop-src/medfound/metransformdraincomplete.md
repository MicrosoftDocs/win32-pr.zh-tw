---
description: 當清空作業完成時，由非同步媒體基礎轉換 (MFT) 傳送。
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: 'METransformDrainComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320475"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="12103-103">METransformDrainComplete 事件</span><span class="sxs-lookup"><span data-stu-id="12103-103">METransformDrainComplete event</span></span>

<span data-ttu-id="12103-104">當清空作業完成時，由非同步媒體基礎轉換 (MFT) 傳送。</span><span class="sxs-lookup"><span data-stu-id="12103-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="12103-105">事件值</span><span class="sxs-lookup"><span data-stu-id="12103-105">Event values</span></span>

<span data-ttu-id="12103-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="12103-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="12103-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="12103-107">VARTYPE</span></span>              | <span data-ttu-id="12103-108">Description</span><span class="sxs-lookup"><span data-stu-id="12103-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="12103-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="12103-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="12103-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="12103-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="12103-111">屬性</span><span class="sxs-lookup"><span data-stu-id="12103-111">Attributes</span></span>

<span data-ttu-id="12103-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="12103-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="12103-113">屬性</span><span class="sxs-lookup"><span data-stu-id="12103-113">Attribute</span></span>                                                                        | <span data-ttu-id="12103-114">描述</span><span class="sxs-lookup"><span data-stu-id="12103-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="12103-115">MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="12103-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="12103-116">已清空的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="12103-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="12103-117">*需要 ()*</span><span class="sxs-lookup"><span data-stu-id="12103-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="12103-118">備註</span><span class="sxs-lookup"><span data-stu-id="12103-118">Remarks</span></span>

<span data-ttu-id="12103-119">非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="12103-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="12103-120">同步 MFTs 不會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="12103-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="12103-121">若要清空 MFT，請使用 **mft \_ 訊息 \_ 命令 \_ 清空** 訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。</span><span class="sxs-lookup"><span data-stu-id="12103-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="12103-122">指定要在 *ulParam* 參數中清空的輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="12103-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="12103-123">清空作業完成時，非同步 MFT 會傳送 METransformDrainComplete 事件。</span><span class="sxs-lookup"><span data-stu-id="12103-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="12103-124">事件的 [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_](mf-event-mft-input-stream-id.md) 識別碼屬性包含 *ulParam* 參數中提供的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="12103-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="12103-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="12103-125">Requirements</span></span>



| <span data-ttu-id="12103-126">需求</span><span class="sxs-lookup"><span data-stu-id="12103-126">Requirement</span></span> | <span data-ttu-id="12103-127">值</span><span class="sxs-lookup"><span data-stu-id="12103-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12103-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12103-128">Minimum supported client</span></span><br/> | <span data-ttu-id="12103-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12103-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="12103-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12103-130">Minimum supported server</span></span><br/> | <span data-ttu-id="12103-131">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12103-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="12103-132">標頭</span><span class="sxs-lookup"><span data-stu-id="12103-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="12103-133"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="12103-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12103-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12103-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12103-135">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="12103-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="12103-136">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="12103-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




