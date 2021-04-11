---
description: 當拓撲的狀態變更時，由媒體會話引發。
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: 'MESessionTopologyStatus 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943797"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="f344c-103">MESessionTopologyStatus 事件</span><span class="sxs-lookup"><span data-stu-id="f344c-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="f344c-104">當拓撲的狀態變更時，由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="f344c-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="f344c-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f344c-105">Event values</span></span>

<span data-ttu-id="f344c-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f344c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f344c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f344c-107">VARTYPE</span></span>                | <span data-ttu-id="f344c-108">Description</span><span class="sxs-lookup"><span data-stu-id="f344c-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f344c-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="f344c-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="f344c-110">拓撲的 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f344c-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="f344c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f344c-111">Attributes</span></span>

<span data-ttu-id="f344c-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f344c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f344c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f344c-113">Attribute</span></span>                                                                            | <span data-ttu-id="f344c-114">描述</span><span class="sxs-lookup"><span data-stu-id="f344c-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f344c-115">**MF \_ 事件 \_ 拓撲 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f344c-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="f344c-116">指定拓撲的新狀態。</span><span class="sxs-lookup"><span data-stu-id="f344c-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f344c-117">備註</span><span class="sxs-lookup"><span data-stu-id="f344c-117">Remarks</span></span>

<span data-ttu-id="f344c-118">如需從事件中抓取 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 指標的程式碼範例，請參閱 [MESessionTopologySet](mesessiontopologyset.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f344c-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f344c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f344c-119">Requirements</span></span>



| <span data-ttu-id="f344c-120">需求</span><span class="sxs-lookup"><span data-stu-id="f344c-120">Requirement</span></span> | <span data-ttu-id="f344c-121">值</span><span class="sxs-lookup"><span data-stu-id="f344c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f344c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f344c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f344c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f344c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f344c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f344c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f344c-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f344c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f344c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f344c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f344c-127"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f344c-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f344c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f344c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f344c-129">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f344c-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




