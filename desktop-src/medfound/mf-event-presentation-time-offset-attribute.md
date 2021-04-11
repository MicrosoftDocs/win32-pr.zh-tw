---
description: 呈現時間與媒體來源時間戳記之間的位移。
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: 'MF_EVENT_PRESENTATION_TIME_OFFSET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848211"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="9daa5-103">MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移屬性</span><span class="sxs-lookup"><span data-stu-id="9daa5-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="9daa5-104">呈現時間與媒體來源時間戳記之間的位移。</span><span class="sxs-lookup"><span data-stu-id="9daa5-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="9daa5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9daa5-105">Data type</span></span>

<span data-ttu-id="9daa5-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="9daa5-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="9daa5-107">備註</span><span class="sxs-lookup"><span data-stu-id="9daa5-107">Remarks</span></span>

<span data-ttu-id="9daa5-108">位移的計算方式如下： offset = presentation time − source time。</span><span class="sxs-lookup"><span data-stu-id="9daa5-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="9daa5-109">這個屬性會搭配下列事件使用：</span><span class="sxs-lookup"><span data-stu-id="9daa5-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="9daa5-110">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="9daa5-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="9daa5-111">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="9daa5-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="9daa5-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9daa5-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9daa5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9daa5-113">Requirements</span></span>



| <span data-ttu-id="9daa5-114">需求</span><span class="sxs-lookup"><span data-stu-id="9daa5-114">Requirement</span></span> | <span data-ttu-id="9daa5-115">值</span><span class="sxs-lookup"><span data-stu-id="9daa5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9daa5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9daa5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9daa5-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9daa5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9daa5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9daa5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9daa5-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9daa5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9daa5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9daa5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9daa5-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9daa5-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9daa5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9daa5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9daa5-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9daa5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9daa5-124">事件屬性</span><span class="sxs-lookup"><span data-stu-id="9daa5-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="9daa5-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="9daa5-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="9daa5-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="9daa5-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




