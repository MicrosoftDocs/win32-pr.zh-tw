---
description: 指定影片媒體類型中的 MPEG-2 或 h.264 設定檔。
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: 'MF_MT_MPEG2_PROFILE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850455"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="4e33c-103">MF \_ MT \_ MPEG2 \_ 配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="4e33c-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="4e33c-104">指定影片媒體類型中的 MPEG-2 或 h.264 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e33c-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e33c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4e33c-105">Data type</span></span>

<span data-ttu-id="4e33c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4e33c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e33c-107">備註</span><span class="sxs-lookup"><span data-stu-id="4e33c-107">Remarks</span></span>

<span data-ttu-id="4e33c-108">針對 MPEG-2 video，這個屬性的值是 [**AM \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="4e33c-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="4e33c-109">若為 h.264 video，此值為 [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="4e33c-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="4e33c-110">這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwProfile** 成員。</span><span class="sxs-lookup"><span data-stu-id="4e33c-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="4e33c-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4e33c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e33c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e33c-112">Requirements</span></span>



| <span data-ttu-id="4e33c-113">需求</span><span class="sxs-lookup"><span data-stu-id="4e33c-113">Requirement</span></span> | <span data-ttu-id="4e33c-114">值</span><span class="sxs-lookup"><span data-stu-id="4e33c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e33c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e33c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4e33c-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e33c-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4e33c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e33c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4e33c-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e33c-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4e33c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4e33c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e33c-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e33c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e33c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e33c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e33c-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4e33c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e33c-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4e33c-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4e33c-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4e33c-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4e33c-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4e33c-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4e33c-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="4e33c-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
