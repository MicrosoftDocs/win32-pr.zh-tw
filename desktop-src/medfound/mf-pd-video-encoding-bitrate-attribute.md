---
description: 指定標記法的影片編碼位元速率（以每秒位數為單位）。 這個屬性會套用至展示描述項。
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: 'MF_PD_VIDEO_ENCODING_BITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985369"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a><span data-ttu-id="5c9a5-104">MF \_ PD \_ VIDEO \_ 編碼 \_ 位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="5c9a5-104">MF\_PD\_VIDEO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="5c9a5-105">指定標記法的影片編碼位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-105">Specifies the video encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="5c9a5-106">這個屬性會套用至展示描述項。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c9a5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="5c9a5-107">Data type</span></span>

<span data-ttu-id="5c9a5-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5c9a5-109">備註</span><span class="sxs-lookup"><span data-stu-id="5c9a5-109">Remarks</span></span>

<span data-ttu-id="5c9a5-110">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-110">This attribute is optional.</span></span> <span data-ttu-id="5c9a5-111">某些格式有更複雜的編碼配置，無法使用這個屬性來匯總。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="5c9a5-112">若為 Advanced Systems Format (ASF) 檔案，下列屬性統稱為編碼位元速率：</span><span class="sxs-lookup"><span data-stu-id="5c9a5-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="5c9a5-113">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最大 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="5c9a5-114">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="5c9a5-115">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大 \_ 資料 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="5c9a5-116">**MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="5c9a5-117">協力廠商格式可能會使用其他自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="5c9a5-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5c9a5-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9a5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c9a5-119">Requirements</span></span>



| <span data-ttu-id="5c9a5-120">需求</span><span class="sxs-lookup"><span data-stu-id="5c9a5-120">Requirement</span></span> | <span data-ttu-id="5c9a5-121">值</span><span class="sxs-lookup"><span data-stu-id="5c9a5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9a5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c9a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9a5-123">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c9a5-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5c9a5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c9a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9a5-125">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c9a5-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5c9a5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5c9a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c9a5-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c9a5-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9a5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c9a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9a5-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5c9a5-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c9a5-130">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5c9a5-131">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5c9a5-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5c9a5-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5c9a5-133">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="5c9a5-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




