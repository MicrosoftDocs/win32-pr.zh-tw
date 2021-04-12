---
description: 影片媒體類型的資料錯誤率（每秒的位錯誤）。
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: 'MF_MT_AVG_BIT_ERROR_RATE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191887"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="13573-103">MF \_ MT \_ 平均 \_ 位 \_ 錯誤率 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="13573-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="13573-104">影片媒體類型的資料錯誤率（每秒的位錯誤）。</span><span class="sxs-lookup"><span data-stu-id="13573-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="13573-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="13573-105">Data type</span></span>

<span data-ttu-id="13573-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="13573-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="13573-107">備註</span><span class="sxs-lookup"><span data-stu-id="13573-107">Remarks</span></span>

<span data-ttu-id="13573-108">這個屬性會對應至 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構的 **dwBitErrorRate** 成員。</span><span class="sxs-lookup"><span data-stu-id="13573-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="13573-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="13573-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="13573-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="13573-110">Requirements</span></span>



| <span data-ttu-id="13573-111">需求</span><span class="sxs-lookup"><span data-stu-id="13573-111">Requirement</span></span> | <span data-ttu-id="13573-112">值</span><span class="sxs-lookup"><span data-stu-id="13573-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13573-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13573-113">Minimum supported client</span></span><br/> | <span data-ttu-id="13573-114">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13573-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="13573-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13573-115">Minimum supported server</span></span><br/> | <span data-ttu-id="13573-116">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13573-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="13573-117">標頭</span><span class="sxs-lookup"><span data-stu-id="13573-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="13573-118"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="13573-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13573-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13573-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13573-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="13573-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="13573-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="13573-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="13573-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="13573-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="13573-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="13573-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="13573-124">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="13573-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
