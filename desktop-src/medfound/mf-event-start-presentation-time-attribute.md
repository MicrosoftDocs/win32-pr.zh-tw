---
description: 簡報的開始時間，以 100-納秒為單位，以呈現時鐘測量。
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: 'MF_EVENT_START_PRESENTATION_TIME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027579"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="62c2a-103">MF \_ 事件 \_ 開始 \_ 簡報 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="62c2a-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="62c2a-104">簡報的開始時間，以 100-納秒為單位，以呈現時鐘測量。</span><span class="sxs-lookup"><span data-stu-id="62c2a-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="62c2a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="62c2a-105">Data type</span></span>

<span data-ttu-id="62c2a-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="62c2a-106">**UINT64**</span></span>

<span data-ttu-id="62c2a-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="62c2a-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c2a-108">備註</span><span class="sxs-lookup"><span data-stu-id="62c2a-108">Remarks</span></span>

<span data-ttu-id="62c2a-109">這個屬性會與 [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="62c2a-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="62c2a-110">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="62c2a-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="62c2a-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="62c2a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c2a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="62c2a-112">Requirements</span></span>



| <span data-ttu-id="62c2a-113">需求</span><span class="sxs-lookup"><span data-stu-id="62c2a-113">Requirement</span></span> | <span data-ttu-id="62c2a-114">值</span><span class="sxs-lookup"><span data-stu-id="62c2a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62c2a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62c2a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="62c2a-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62c2a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="62c2a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62c2a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="62c2a-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62c2a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62c2a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="62c2a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c2a-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="62c2a-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c2a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62c2a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c2a-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="62c2a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62c2a-123">事件屬性</span><span class="sxs-lookup"><span data-stu-id="62c2a-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="62c2a-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="62c2a-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="62c2a-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="62c2a-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




