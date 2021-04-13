---
description: 包含媒體來源從其目前位置重新開機的開始時間。
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: 'MF_EVENT_SOURCE_ACTUAL_START 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386173"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="6c2e9-103">MF \_ 事件 \_ 來源 \_ 實際 \_ 開始屬性</span><span class="sxs-lookup"><span data-stu-id="6c2e9-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="6c2e9-104">包含媒體來源從其目前位置重新開機的開始時間。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c2e9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6c2e9-105">Data type</span></span>

<span data-ttu-id="6c2e9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="6c2e9-106">**UINT64**</span></span>

<span data-ttu-id="6c2e9-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2e9-108">備註</span><span class="sxs-lookup"><span data-stu-id="6c2e9-108">Remarks</span></span>

<span data-ttu-id="6c2e9-109">這個屬性會與 [MESourceStarted](mesourcestarted.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="6c2e9-110">當事件資料為空白 (**VT \_ 空白**) （表示媒體來源從目前的播放位置開始）時，屬性就會相關。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="6c2e9-111">在此情況下， **MF \_ 事件 \_ 來源 \_ 實際 \_ 開始** 屬性會指定實際的開始時間。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="6c2e9-112">如果事件資料是 **VT \_ 空** 的，而且未設定此屬性，則開始時間會假設為零。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="6c2e9-113">當 [MESourceStarted](mesourcestarted.md) 的事件資料包含開始時間 (**VT \_ I8**) 時，不應設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="6c2e9-114">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="6c2e9-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6c2e9-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2e9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c2e9-116">Requirements</span></span>



| <span data-ttu-id="6c2e9-117">需求</span><span class="sxs-lookup"><span data-stu-id="6c2e9-117">Requirement</span></span> | <span data-ttu-id="6c2e9-118">值</span><span class="sxs-lookup"><span data-stu-id="6c2e9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2e9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c2e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2e9-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2e9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6c2e9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c2e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2e9-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2e9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c2e9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6c2e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c2e9-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c2e9-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2e9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c2e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2e9-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6c2e9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c2e9-127">事件屬性</span><span class="sxs-lookup"><span data-stu-id="6c2e9-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c2e9-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="6c2e9-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="6c2e9-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="6c2e9-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




