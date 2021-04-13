---
description: 影片媒體類型的大約影片資料流程資料速率（以每秒位數為單位）。
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: 'MF_MT_AVG_BITRATE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386269"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="ca0b4-103">MF \_ MT \_ 平均 \_ 位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="ca0b4-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="ca0b4-104">影片媒體類型的大約影片資料流程資料速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="ca0b4-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca0b4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ca0b4-105">Data type</span></span>

<span data-ttu-id="ca0b4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ca0b4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ca0b4-107">備註</span><span class="sxs-lookup"><span data-stu-id="ca0b4-107">Remarks</span></span>

<span data-ttu-id="ca0b4-108">這個屬性會對應至 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構的 **dwBitRate** 成員。</span><span class="sxs-lookup"><span data-stu-id="ca0b4-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="ca0b4-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ca0b4-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca0b4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca0b4-110">Requirements</span></span>



| <span data-ttu-id="ca0b4-111">需求</span><span class="sxs-lookup"><span data-stu-id="ca0b4-111">Requirement</span></span> | <span data-ttu-id="ca0b4-112">值</span><span class="sxs-lookup"><span data-stu-id="ca0b4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0b4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca0b4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0b4-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca0b4-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ca0b4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca0b4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0b4-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca0b4-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ca0b4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ca0b4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0b4-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca0b4-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca0b4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca0b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0b4-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ca0b4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ca0b4-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ca0b4-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ca0b4-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ca0b4-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ca0b4-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ca0b4-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ca0b4-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="ca0b4-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
