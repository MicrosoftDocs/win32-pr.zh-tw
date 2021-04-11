---
description: 在呼叫 IMFStreamSink：:P laceMarker 方法之後，由資料流程接收器引發。
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: 'MEStreamSinkMarker 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691824"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="8fa3f-103">MEStreamSinkMarker 事件</span><span class="sxs-lookup"><span data-stu-id="8fa3f-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="8fa3f-104">在呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法之後，由資料流程接收器引發。</span><span class="sxs-lookup"><span data-stu-id="8fa3f-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="8fa3f-105">事件值</span><span class="sxs-lookup"><span data-stu-id="8fa3f-105">Event values</span></span>

<span data-ttu-id="8fa3f-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="8fa3f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8fa3f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8fa3f-107">VARTYPE</span></span>            | <span data-ttu-id="8fa3f-108">Description</span><span class="sxs-lookup"><span data-stu-id="8fa3f-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa3f-109">>任何</span><span class="sxs-lookup"><span data-stu-id="8fa3f-109">>Any</span></span><br/> | <span data-ttu-id="8fa3f-110">事件值是呼叫端在 [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)方法的 *pvarCoNtextValue* 參數中指定的 **PROPVARIANT** 複本。</span><span class="sxs-lookup"><span data-stu-id="8fa3f-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="8fa3f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fa3f-111">Requirements</span></span>



| <span data-ttu-id="8fa3f-112">需求</span><span class="sxs-lookup"><span data-stu-id="8fa3f-112">Requirement</span></span> | <span data-ttu-id="8fa3f-113">值</span><span class="sxs-lookup"><span data-stu-id="8fa3f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa3f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fa3f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa3f-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa3f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fa3f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fa3f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa3f-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa3f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fa3f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8fa3f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fa3f-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="8fa3f-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa3f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fa3f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa3f-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="8fa3f-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="8fa3f-122">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="8fa3f-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




