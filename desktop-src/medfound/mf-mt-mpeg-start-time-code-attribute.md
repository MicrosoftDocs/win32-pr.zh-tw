---
description: 適用于 MPEG-2 或 MPEG-2 影片媒體類型的圖片群組 (GOP) 開始時間代碼。
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: 'MF_MT_MPEG_START_TIME_CODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990340"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="53561-103">MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼屬性</span><span class="sxs-lookup"><span data-stu-id="53561-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="53561-104">適用于 MPEG-2 或 MPEG-2 影片媒體類型的圖片群組 (GOP) 開始時間代碼。</span><span class="sxs-lookup"><span data-stu-id="53561-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="53561-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="53561-105">Data type</span></span>

<span data-ttu-id="53561-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53561-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="53561-107">備註</span><span class="sxs-lookup"><span data-stu-id="53561-107">Remarks</span></span>

<span data-ttu-id="53561-108">這個屬性會對應至 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)和 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwStartTimeCode** 成員。</span><span class="sxs-lookup"><span data-stu-id="53561-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="53561-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="53561-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="53561-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="53561-110">Requirements</span></span>



| <span data-ttu-id="53561-111">需求</span><span class="sxs-lookup"><span data-stu-id="53561-111">Requirement</span></span> | <span data-ttu-id="53561-112">值</span><span class="sxs-lookup"><span data-stu-id="53561-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53561-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53561-113">Minimum supported client</span></span><br/> | <span data-ttu-id="53561-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53561-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="53561-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53561-115">Minimum supported server</span></span><br/> | <span data-ttu-id="53561-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53561-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="53561-117">標頭</span><span class="sxs-lookup"><span data-stu-id="53561-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="53561-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="53561-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53561-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53561-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53561-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="53561-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="53561-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53561-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="53561-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="53561-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="53561-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="53561-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="53561-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="53561-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="53561-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="53561-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
