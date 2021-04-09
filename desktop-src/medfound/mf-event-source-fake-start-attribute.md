---
description: 指定目前區段拓撲是否為空白。
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: 'MF_EVENT_SOURCE_FAKE_START 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853003"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="6e43d-103">MF \_ 事件 \_ 來源 \_ 假 \_ 開始屬性</span><span class="sxs-lookup"><span data-stu-id="6e43d-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="6e43d-104">指定目前區段拓撲是否為空白。</span><span class="sxs-lookup"><span data-stu-id="6e43d-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e43d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6e43d-105">Data type</span></span>

<span data-ttu-id="6e43d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6e43d-106">**UINT32**</span></span>

<span data-ttu-id="6e43d-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="6e43d-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e43d-108">備註</span><span class="sxs-lookup"><span data-stu-id="6e43d-108">Remarks</span></span>

<span data-ttu-id="6e43d-109">這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="6e43d-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="6e43d-110">如果目前區段拓撲是空的，sequencer 來源會將這個屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6e43d-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="6e43d-111">如果此屬性為 **TRUE**，表示尚未開始播放。</span><span class="sxs-lookup"><span data-stu-id="6e43d-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="6e43d-112">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6e43d-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="6e43d-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6e43d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e43d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e43d-114">Requirements</span></span>



| <span data-ttu-id="6e43d-115">需求</span><span class="sxs-lookup"><span data-stu-id="6e43d-115">Requirement</span></span> | <span data-ttu-id="6e43d-116">值</span><span class="sxs-lookup"><span data-stu-id="6e43d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e43d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e43d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e43d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e43d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e43d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e43d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e43d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e43d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e43d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6e43d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e43d-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e43d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e43d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e43d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e43d-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6e43d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e43d-125">事件屬性</span><span class="sxs-lookup"><span data-stu-id="6e43d-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e43d-126">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6e43d-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6e43d-127">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6e43d-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




