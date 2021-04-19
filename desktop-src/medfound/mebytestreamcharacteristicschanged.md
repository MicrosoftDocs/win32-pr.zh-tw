---
description: 當位元組資料流程的特性變更時，由位元組資料流程傳送。
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: 'MEByteStreamCharacteristicsChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001348"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="30eda-103">MEByteStreamCharacteristicsChanged 事件</span><span class="sxs-lookup"><span data-stu-id="30eda-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="30eda-104">當位元組資料流程的特性變更時，由位元組資料流程傳送。</span><span class="sxs-lookup"><span data-stu-id="30eda-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="30eda-105">事件值</span><span class="sxs-lookup"><span data-stu-id="30eda-105">Event values</span></span>

<span data-ttu-id="30eda-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="30eda-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="30eda-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="30eda-107">VARTYPE</span></span>               | <span data-ttu-id="30eda-108">Description</span><span class="sxs-lookup"><span data-stu-id="30eda-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="30eda-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="30eda-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="30eda-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="30eda-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="30eda-111">備註</span><span class="sxs-lookup"><span data-stu-id="30eda-111">Remarks</span></span>

<span data-ttu-id="30eda-112">此事件表示下列一或多個特性已變更：</span><span class="sxs-lookup"><span data-stu-id="30eda-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="30eda-113">功能旗標 ([**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities)) </span><span class="sxs-lookup"><span data-stu-id="30eda-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="30eda-114">資料流程結尾旗標 ([**IMFByteStream：： IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream)) </span><span class="sxs-lookup"><span data-stu-id="30eda-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="30eda-115">Length ([**IMFByteStream：： GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength)) </span><span class="sxs-lookup"><span data-stu-id="30eda-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="30eda-116">並非所有的 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 執行都支援此事件。</span><span class="sxs-lookup"><span data-stu-id="30eda-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="30eda-117">若要接收事件，請查詢 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面的位元組資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="30eda-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="30eda-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="30eda-118">Requirements</span></span>



| <span data-ttu-id="30eda-119">需求</span><span class="sxs-lookup"><span data-stu-id="30eda-119">Requirement</span></span> | <span data-ttu-id="30eda-120">值</span><span class="sxs-lookup"><span data-stu-id="30eda-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30eda-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30eda-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30eda-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30eda-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="30eda-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30eda-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30eda-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30eda-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30eda-125">標頭</span><span class="sxs-lookup"><span data-stu-id="30eda-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="30eda-126"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="30eda-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30eda-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30eda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30eda-128">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="30eda-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




