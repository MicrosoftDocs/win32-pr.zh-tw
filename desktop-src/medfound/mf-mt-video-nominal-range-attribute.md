---
description: 指定影片媒體類型中色彩資訊的名義範圍。
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: 'MF_MT_VIDEO_NOMINAL_RANGE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986603"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="1aecb-103">MF \_ MT \_ 影片 \_ 名義 \_ 範圍屬性</span><span class="sxs-lookup"><span data-stu-id="1aecb-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="1aecb-104">指定影片媒體類型中色彩資訊的名義範圍。</span><span class="sxs-lookup"><span data-stu-id="1aecb-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1aecb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1aecb-105">Data type</span></span>

<span data-ttu-id="1aecb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1aecb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1aecb-107">備註</span><span class="sxs-lookup"><span data-stu-id="1aecb-107">Remarks</span></span>

<span data-ttu-id="1aecb-108">這個屬性的值是 [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="1aecb-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="1aecb-109">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1aecb-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="1aecb-110">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="1aecb-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="1aecb-111">在輸出媒體類型上，您 \_ \_ \_ \_ 可以使用 **MFNominalRange \_ 0 \_ 255** 和 **MFNominalRange \_ 16 \_ 235** 設定 MF MT 影片名義範圍。</span><span class="sxs-lookup"><span data-stu-id="1aecb-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="1aecb-112">H.264/AVC 編碼器應該將 **MFNominalRange \_ Unknown** 視為 **MFNominalRange \_ 16 \_ 235**。</span><span class="sxs-lookup"><span data-stu-id="1aecb-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="1aecb-113">當 MF \_ MT \_ \_ 的視頻名義 \_ 範圍設定為 **MFNominalRange \_ 48 \_ 208**、 **MFNominalRange \_ 64 \_ 127** 或 [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)未定義的任何其他值時，h.264/AVC 編碼器應拒絕輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1aecb-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aecb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aecb-114">Requirements</span></span>



| <span data-ttu-id="1aecb-115">需求</span><span class="sxs-lookup"><span data-stu-id="1aecb-115">Requirement</span></span> | <span data-ttu-id="1aecb-116">值</span><span class="sxs-lookup"><span data-stu-id="1aecb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aecb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aecb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1aecb-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aecb-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1aecb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aecb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1aecb-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aecb-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1aecb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1aecb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aecb-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1aecb-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aecb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aecb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aecb-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1aecb-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1aecb-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1aecb-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1aecb-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1aecb-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1aecb-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1aecb-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1aecb-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="1aecb-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="1aecb-129">擴充的色彩資訊</span><span class="sxs-lookup"><span data-stu-id="1aecb-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




