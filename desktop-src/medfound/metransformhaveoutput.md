---
description: 當從 MFT 提供新的輸出資料時，由非同步媒體基礎轉換 (MFT) 。
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: 'METransformHaveOutput 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972253"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="4d982-103">METransformHaveOutput 事件</span><span class="sxs-lookup"><span data-stu-id="4d982-103">METransformHaveOutput event</span></span>

<span data-ttu-id="4d982-104">當從 MFT 提供新的輸出資料時，由非同步媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="4d982-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="4d982-105">事件值</span><span class="sxs-lookup"><span data-stu-id="4d982-105">Event values</span></span>

<span data-ttu-id="4d982-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="4d982-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4d982-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4d982-107">VARTYPE</span></span>              | <span data-ttu-id="4d982-108">Description</span><span class="sxs-lookup"><span data-stu-id="4d982-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="4d982-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="4d982-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4d982-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="4d982-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4d982-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4d982-111">Attributes</span></span>

<span data-ttu-id="4d982-112">未定義此事件的屬性。</span><span class="sxs-lookup"><span data-stu-id="4d982-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d982-113">備註</span><span class="sxs-lookup"><span data-stu-id="4d982-113">Remarks</span></span>

<span data-ttu-id="4d982-114">非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="4d982-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="4d982-115">同步 MFTs 不會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="4d982-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="4d982-116">當 MFT 用戶端收到此事件時，它應該呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來取得輸出。</span><span class="sxs-lookup"><span data-stu-id="4d982-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d982-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d982-117">Requirements</span></span>



| <span data-ttu-id="4d982-118">需求</span><span class="sxs-lookup"><span data-stu-id="4d982-118">Requirement</span></span> | <span data-ttu-id="4d982-119">值</span><span class="sxs-lookup"><span data-stu-id="4d982-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d982-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d982-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d982-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d982-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4d982-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d982-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d982-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d982-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="4d982-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4d982-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d982-125"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="4d982-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d982-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d982-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d982-127">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="4d982-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4d982-128">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="4d982-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




