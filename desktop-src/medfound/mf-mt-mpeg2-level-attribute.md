---
description: 指定影片媒體類型中的 MPEG-2 或 h.264 層級。
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: 'MF_MT_MPEG2_LEVEL 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193628"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="a8408-103">MF \_ MT \_ MPEG2 \_ 層級屬性</span><span class="sxs-lookup"><span data-stu-id="a8408-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="a8408-104">指定影片媒體類型中的 MPEG-2 或 h.264 層級。</span><span class="sxs-lookup"><span data-stu-id="a8408-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8408-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a8408-105">Data type</span></span>

<span data-ttu-id="a8408-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a8408-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8408-107">備註</span><span class="sxs-lookup"><span data-stu-id="a8408-107">Remarks</span></span>

<span data-ttu-id="a8408-108">針對 MPEG-2 video，這個屬性的值是 [**AM \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="a8408-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="a8408-109">若為 h.264 video，此值為 [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="a8408-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="a8408-110">這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwLevel** 成員。</span><span class="sxs-lookup"><span data-stu-id="a8408-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="a8408-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a8408-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8408-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8408-112">Requirements</span></span>



| <span data-ttu-id="a8408-113">需求</span><span class="sxs-lookup"><span data-stu-id="a8408-113">Requirement</span></span> | <span data-ttu-id="a8408-114">值</span><span class="sxs-lookup"><span data-stu-id="a8408-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8408-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8408-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a8408-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8408-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a8408-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8408-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a8408-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8408-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a8408-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a8408-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8408-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8408-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8408-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8408-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8408-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a8408-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8408-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a8408-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a8408-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a8408-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a8408-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a8408-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a8408-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="a8408-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
