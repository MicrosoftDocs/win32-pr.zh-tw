---
description: 當資料流程的媒體類型變更時，由媒體資料流程引發。
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: 'MEStreamFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848533"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="9a751-103">MEStreamFormatChanged 事件</span><span class="sxs-lookup"><span data-stu-id="9a751-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="9a751-104">當資料流程的媒體類型變更時，由媒體資料流程引發。</span><span class="sxs-lookup"><span data-stu-id="9a751-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="9a751-105">事件值</span><span class="sxs-lookup"><span data-stu-id="9a751-105">Event values</span></span>

<span data-ttu-id="9a751-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="9a751-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9a751-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9a751-107">VARTYPE</span></span>                | <span data-ttu-id="9a751-108">Description</span><span class="sxs-lookup"><span data-stu-id="9a751-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a751-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="9a751-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9a751-110">新媒體類型之 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9a751-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9a751-111">備註</span><span class="sxs-lookup"><span data-stu-id="9a751-111">Remarks</span></span>

<span data-ttu-id="9a751-112">您可以使用此事件來通知資料流程中的格式變更。</span><span class="sxs-lookup"><span data-stu-id="9a751-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a751-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a751-113">Requirements</span></span>



| <span data-ttu-id="9a751-114">需求</span><span class="sxs-lookup"><span data-stu-id="9a751-114">Requirement</span></span> | <span data-ttu-id="9a751-115">值</span><span class="sxs-lookup"><span data-stu-id="9a751-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a751-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a751-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a751-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a751-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a751-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a751-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a751-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a751-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9a751-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9a751-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a751-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="9a751-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a751-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a751-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a751-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="9a751-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




