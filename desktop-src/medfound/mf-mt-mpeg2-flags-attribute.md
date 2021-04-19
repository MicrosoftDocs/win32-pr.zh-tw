---
description: 包含 MPEG-2 影片媒體類型的其他旗標。
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: 'MF_MT_MPEG2_FLAGS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997953"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="3fc4e-103">MF \_ MT \_ MPEG2 \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="3fc4e-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="3fc4e-104">包含 MPEG-2 影片媒體類型的其他旗標。</span><span class="sxs-lookup"><span data-stu-id="3fc4e-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="3fc4e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3fc4e-105">Data type</span></span>

<span data-ttu-id="3fc4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc4e-107">備註</span><span class="sxs-lookup"><span data-stu-id="3fc4e-107">Remarks</span></span>

<span data-ttu-id="3fc4e-108">這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="3fc4e-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="3fc4e-109">如需有效旗標的清單，請參閱 **MPEG2VIDEOINFO** 的檔。</span><span class="sxs-lookup"><span data-stu-id="3fc4e-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="3fc4e-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3fc4e-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc4e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fc4e-111">Requirements</span></span>



| <span data-ttu-id="3fc4e-112">需求</span><span class="sxs-lookup"><span data-stu-id="3fc4e-112">Requirement</span></span> | <span data-ttu-id="3fc4e-113">值</span><span class="sxs-lookup"><span data-stu-id="3fc4e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc4e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fc4e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc4e-115">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fc4e-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3fc4e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fc4e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc4e-117">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fc4e-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3fc4e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3fc4e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc4e-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc4e-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc4e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fc4e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc4e-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3fc4e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3fc4e-122">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3fc4e-123">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3fc4e-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3fc4e-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="3fc4e-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="3fc4e-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
