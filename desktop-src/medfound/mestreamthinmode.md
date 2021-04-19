---
description: 由媒體資料流程啟動或停止 thinning 資料流程時引發。 如需 thinning 的詳細資訊，請參閱關於速率控制。
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: 'MEStreamThinMode 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969270"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="de4e5-104">MEStreamThinMode 事件</span><span class="sxs-lookup"><span data-stu-id="de4e5-104">MEStreamThinMode event</span></span>

<span data-ttu-id="de4e5-105">由媒體資料流程啟動或停止 thinning 資料流程時引發。</span><span class="sxs-lookup"><span data-stu-id="de4e5-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="de4e5-106">如需 *thinning* 的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="de4e5-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="de4e5-107">您可以傳送此事件以回應 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法或 [**IMFQualityAdvise：： SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) 方法。</span><span class="sxs-lookup"><span data-stu-id="de4e5-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="de4e5-108">事件值</span><span class="sxs-lookup"><span data-stu-id="de4e5-108">Event values</span></span>

<span data-ttu-id="de4e5-109">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="de4e5-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de4e5-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="de4e5-110">VARTYPE</span></span></th>
<th><span data-ttu-id="de4e5-111">Description</span><span class="sxs-lookup"><span data-stu-id="de4e5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de4e5-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="de4e5-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="de4e5-113">指出 thinning 是否已啟動或停止。</span><span class="sxs-lookup"><span data-stu-id="de4e5-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="de4e5-114">VARIANT_TRUE： thinned 此事件之後傳遞的範例。</span><span class="sxs-lookup"><span data-stu-id="de4e5-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="de4e5-115">VARIANT_FALSE：未 thinned 此事件之後傳遞的範例。</span><span class="sxs-lookup"><span data-stu-id="de4e5-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="de4e5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="de4e5-116">Requirements</span></span>



| <span data-ttu-id="de4e5-117">需求</span><span class="sxs-lookup"><span data-stu-id="de4e5-117">Requirement</span></span> | <span data-ttu-id="de4e5-118">值</span><span class="sxs-lookup"><span data-stu-id="de4e5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4e5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de4e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de4e5-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de4e5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de4e5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de4e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de4e5-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de4e5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de4e5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="de4e5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de4e5-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="de4e5-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4e5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de4e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4e5-126">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="de4e5-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




