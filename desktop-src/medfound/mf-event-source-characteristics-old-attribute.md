---
description: 指定媒體來源的先前特性。
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: 'MF_EVENT_SOURCE_CHARACTERISTICS_OLD 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975000"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="dfd36-103">MF \_ 事件 \_ 來源 \_ 特性 \_ 舊屬性</span><span class="sxs-lookup"><span data-stu-id="dfd36-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="dfd36-104">指定媒體來源的先前特性。</span><span class="sxs-lookup"><span data-stu-id="dfd36-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="dfd36-105">屬性資料是 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)列舉中的位 **或** 旗標。</span><span class="sxs-lookup"><span data-stu-id="dfd36-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="dfd36-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="dfd36-106">Data type</span></span>

<span data-ttu-id="dfd36-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dfd36-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd36-108">備註</span><span class="sxs-lookup"><span data-stu-id="dfd36-108">Remarks</span></span>

<span data-ttu-id="dfd36-109">這個屬性會與 [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="dfd36-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="dfd36-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="dfd36-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd36-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfd36-111">Requirements</span></span>



| <span data-ttu-id="dfd36-112">需求</span><span class="sxs-lookup"><span data-stu-id="dfd36-112">Requirement</span></span> | <span data-ttu-id="dfd36-113">值</span><span class="sxs-lookup"><span data-stu-id="dfd36-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd36-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfd36-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd36-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfd36-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dfd36-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfd36-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd36-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfd36-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dfd36-118">標頭</span><span class="sxs-lookup"><span data-stu-id="dfd36-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfd36-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd36-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd36-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfd36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd36-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="dfd36-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dfd36-122">事件屬性</span><span class="sxs-lookup"><span data-stu-id="dfd36-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="dfd36-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dfd36-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dfd36-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dfd36-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dfd36-125">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="dfd36-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




