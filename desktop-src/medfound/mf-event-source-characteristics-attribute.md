---
description: 指定媒體來源的目前特性。
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: 'MF_EVENT_SOURCE_CHARACTERISTICS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974071"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="1560f-103">MF \_ 事件 \_ 來源 \_ 特性屬性</span><span class="sxs-lookup"><span data-stu-id="1560f-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="1560f-104">指定媒體來源的目前特性。</span><span class="sxs-lookup"><span data-stu-id="1560f-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="1560f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1560f-105">Data type</span></span>

<span data-ttu-id="1560f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1560f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1560f-107">備註</span><span class="sxs-lookup"><span data-stu-id="1560f-107">Remarks</span></span>

<span data-ttu-id="1560f-108">這個屬性的值是 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)列舉中的位 **or** of 旗標。</span><span class="sxs-lookup"><span data-stu-id="1560f-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="1560f-109">這個屬性會與 [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="1560f-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="1560f-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1560f-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1560f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1560f-111">Requirements</span></span>



| <span data-ttu-id="1560f-112">需求</span><span class="sxs-lookup"><span data-stu-id="1560f-112">Requirement</span></span> | <span data-ttu-id="1560f-113">值</span><span class="sxs-lookup"><span data-stu-id="1560f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1560f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1560f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1560f-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1560f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1560f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1560f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1560f-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1560f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1560f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1560f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1560f-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1560f-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1560f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1560f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1560f-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1560f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1560f-122">事件屬性</span><span class="sxs-lookup"><span data-stu-id="1560f-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1560f-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1560f-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1560f-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1560f-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




