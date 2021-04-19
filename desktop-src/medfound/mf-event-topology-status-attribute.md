---
description: 指定播放期間拓撲的狀態。
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: 'MF_EVENT_TOPOLOGY_STATUS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998913"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="3a243-103">MF \_ 事件 \_ 拓撲 \_ 狀態屬性</span><span class="sxs-lookup"><span data-stu-id="3a243-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="3a243-104">指定播放期間拓撲的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a243-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a243-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3a243-105">Data type</span></span>

<span data-ttu-id="3a243-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a243-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a243-107">備註</span><span class="sxs-lookup"><span data-stu-id="3a243-107">Remarks</span></span>

<span data-ttu-id="3a243-108">這個屬性的值是 [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="3a243-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="3a243-109">這個屬性會與 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="3a243-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="3a243-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3a243-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a243-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a243-111">Requirements</span></span>



| <span data-ttu-id="3a243-112">需求</span><span class="sxs-lookup"><span data-stu-id="3a243-112">Requirement</span></span> | <span data-ttu-id="3a243-113">值</span><span class="sxs-lookup"><span data-stu-id="3a243-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a243-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a243-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3a243-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a243-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a243-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a243-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3a243-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a243-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a243-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3a243-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a243-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a243-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a243-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a243-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a243-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3a243-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a243-122">事件屬性</span><span class="sxs-lookup"><span data-stu-id="3a243-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a243-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a243-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3a243-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a243-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




