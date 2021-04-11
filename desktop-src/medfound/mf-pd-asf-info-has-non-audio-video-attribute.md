---
description: 指定 Advanced Systems 格式 (ASF) 檔案是否包含非音訊或影片的任何資料流程。
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: 'MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944687"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="064eb-103">MF \_ PD \_ ASF \_ 資訊 \_ 具有 \_ 非 \_ 音訊 \_ 影片屬性</span><span class="sxs-lookup"><span data-stu-id="064eb-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="064eb-104">指定 Advanced Systems 格式 (ASF) 檔案是否包含非音訊或影片的任何資料流程。</span><span class="sxs-lookup"><span data-stu-id="064eb-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="064eb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="064eb-105">Data type</span></span>

<span data-ttu-id="064eb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="064eb-106">**UINT32**</span></span>

<span data-ttu-id="064eb-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="064eb-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="064eb-108">備註</span><span class="sxs-lookup"><span data-stu-id="064eb-108">Remarks</span></span>

<span data-ttu-id="064eb-109">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="064eb-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="064eb-110">如果值為 **TRUE**，表示檔案至少有一個非音訊或影片的資料流程。</span><span class="sxs-lookup"><span data-stu-id="064eb-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="064eb-111">範例包括影像串流、指令碼命令和自訂任意資料。</span><span class="sxs-lookup"><span data-stu-id="064eb-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="064eb-112">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="064eb-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="064eb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="064eb-113">Requirements</span></span>



| <span data-ttu-id="064eb-114">需求</span><span class="sxs-lookup"><span data-stu-id="064eb-114">Requirement</span></span> | <span data-ttu-id="064eb-115">值</span><span class="sxs-lookup"><span data-stu-id="064eb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="064eb-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="064eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="064eb-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="064eb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="064eb-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="064eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="064eb-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="064eb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="064eb-120">標頭</span><span class="sxs-lookup"><span data-stu-id="064eb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="064eb-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="064eb-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064eb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="064eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064eb-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="064eb-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="064eb-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="064eb-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="064eb-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="064eb-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="064eb-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="064eb-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="064eb-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="064eb-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="064eb-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="064eb-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




