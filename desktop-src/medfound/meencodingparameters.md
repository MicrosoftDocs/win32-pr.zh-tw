---
description: 由管線傳送至編碼器 MFTs，並透過 IMFTransform：:P rocessEvent 以媒體範例順序傳送。
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: 'MEEncodingParameters 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191914"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="bafd9-103">MEEncodingParameters 事件</span><span class="sxs-lookup"><span data-stu-id="bafd9-103">MEEncodingParameters event</span></span>

<span data-ttu-id="bafd9-104">由管線傳送至編碼器 MFTs，並透過 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)以媒體範例順序傳送。</span><span class="sxs-lookup"><span data-stu-id="bafd9-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="bafd9-105">事件值</span><span class="sxs-lookup"><span data-stu-id="bafd9-105">Event values</span></span>

<span data-ttu-id="bafd9-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="bafd9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bafd9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bafd9-107">VARTYPE</span></span>              | <span data-ttu-id="bafd9-108">Description</span><span class="sxs-lookup"><span data-stu-id="bafd9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="bafd9-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="bafd9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bafd9-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="bafd9-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="bafd9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bafd9-111">Attributes</span></span>

<span data-ttu-id="bafd9-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="bafd9-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="bafd9-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bafd9-113">Attribute</span></span>                                         | <span data-ttu-id="bafd9-114">描述</span><span class="sxs-lookup"><span data-stu-id="bafd9-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bafd9-115">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="bafd9-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="bafd9-116">包含新的 ICodecAPI 為基礎的設定，此設定會在後續的傳入範例上套用編碼器。</span><span class="sxs-lookup"><span data-stu-id="bafd9-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bafd9-117">備註</span><span class="sxs-lookup"><span data-stu-id="bafd9-117">Remarks</span></span>

<span data-ttu-id="bafd9-118">事件承載是 (IMFAttributes 指標) 的屬性存放區，其中包含編碼器應該在後續的傳入範例上套用的新 ICodecAPI 型///設定。</span><span class="sxs-lookup"><span data-stu-id="bafd9-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="bafd9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bafd9-119">Requirements</span></span>



| <span data-ttu-id="bafd9-120">需求</span><span class="sxs-lookup"><span data-stu-id="bafd9-120">Requirement</span></span> | <span data-ttu-id="bafd9-121">值</span><span class="sxs-lookup"><span data-stu-id="bafd9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bafd9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bafd9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bafd9-123">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bafd9-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bafd9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bafd9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bafd9-125">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bafd9-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="bafd9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bafd9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bafd9-127"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="bafd9-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bafd9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bafd9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafd9-129">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="bafd9-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




