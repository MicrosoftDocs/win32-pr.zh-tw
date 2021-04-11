---
description: 指定區段拓撲的開始時間。
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: 'MF_EVENT_SOURCE_PROJECTSTART 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853000"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="4127d-103">MF \_ 事件 \_ 來源 \_ PROJECTSTART 屬性</span><span class="sxs-lookup"><span data-stu-id="4127d-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="4127d-104">指定區段拓撲的開始時間。</span><span class="sxs-lookup"><span data-stu-id="4127d-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="4127d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4127d-105">Data type</span></span>

<span data-ttu-id="4127d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4127d-106">**UINT64**</span></span>

<span data-ttu-id="4127d-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="4127d-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4127d-108">備註</span><span class="sxs-lookup"><span data-stu-id="4127d-108">Remarks</span></span>

<span data-ttu-id="4127d-109">這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="4127d-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="4127d-110">當目前區段拓撲具有 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 屬性時，sequencer 來源會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4127d-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="4127d-111">這兩個屬性具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="4127d-111">The two attributes have the same value.</span></span>

<span data-ttu-id="4127d-112">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="4127d-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="4127d-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4127d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4127d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4127d-114">Requirements</span></span>



| <span data-ttu-id="4127d-115">需求</span><span class="sxs-lookup"><span data-stu-id="4127d-115">Requirement</span></span> | <span data-ttu-id="4127d-116">值</span><span class="sxs-lookup"><span data-stu-id="4127d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4127d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4127d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4127d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4127d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4127d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4127d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4127d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4127d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4127d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4127d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4127d-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4127d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4127d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4127d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4127d-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4127d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4127d-125">事件屬性</span><span class="sxs-lookup"><span data-stu-id="4127d-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4127d-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4127d-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4127d-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="4127d-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




