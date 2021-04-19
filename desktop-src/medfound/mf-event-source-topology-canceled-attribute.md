---
description: 指定 Sequencer 來源是否取消拓撲。
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: 'MF_EVENT_SOURCE_TOPOLOGY_CANCELED 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976362"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="6ca7e-103">MF \_ 事件 \_ 來源 \_ 拓撲 \_ 已取消屬性</span><span class="sxs-lookup"><span data-stu-id="6ca7e-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="6ca7e-104">指定 [Sequencer 來源](sequencer-source.md) 是否取消拓撲。</span><span class="sxs-lookup"><span data-stu-id="6ca7e-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="6ca7e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6ca7e-105">Data type</span></span>

<span data-ttu-id="6ca7e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-106">**UINT32**</span></span>

<span data-ttu-id="6ca7e-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="6ca7e-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca7e-108">備註</span><span class="sxs-lookup"><span data-stu-id="6ca7e-108">Remarks</span></span>

<span data-ttu-id="6ca7e-109">這個屬性會搭配下列事件使用：</span><span class="sxs-lookup"><span data-stu-id="6ca7e-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="6ca7e-110">MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="6ca7e-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="6ca7e-111">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="6ca7e-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="6ca7e-112">如果這個屬性存在且為非零值，表示因為 sequencer 來源取消了拓撲，所以表示呈現區段已結束。</span><span class="sxs-lookup"><span data-stu-id="6ca7e-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="6ca7e-113">否則，表示區段會正常地結束。</span><span class="sxs-lookup"><span data-stu-id="6ca7e-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="6ca7e-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6ca7e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca7e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ca7e-115">Requirements</span></span>



| <span data-ttu-id="6ca7e-116">需求</span><span class="sxs-lookup"><span data-stu-id="6ca7e-116">Requirement</span></span> | <span data-ttu-id="6ca7e-117">值</span><span class="sxs-lookup"><span data-stu-id="6ca7e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca7e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ca7e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca7e-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ca7e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ca7e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ca7e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca7e-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ca7e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ca7e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6ca7e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca7e-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca7e-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca7e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ca7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca7e-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6ca7e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ca7e-126">事件屬性</span><span class="sxs-lookup"><span data-stu-id="6ca7e-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6ca7e-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6ca7e-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6ca7e-129">Sequencer 來源事件</span><span class="sxs-lookup"><span data-stu-id="6ca7e-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




