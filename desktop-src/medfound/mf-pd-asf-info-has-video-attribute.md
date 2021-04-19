---
description: 指定 Advanced Systems Format (ASF) 檔案是否至少包含一個影片串流。
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: 'MF_PD_ASF_INFO_HAS_VIDEO 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995854"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="83ca2-103">MF \_ PD \_ ASF \_ 資訊 \_ 有 \_ 影片屬性</span><span class="sxs-lookup"><span data-stu-id="83ca2-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="83ca2-104">指定 Advanced Systems Format (ASF) 檔案是否至少包含一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="83ca2-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="83ca2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="83ca2-105">Data type</span></span>

<span data-ttu-id="83ca2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="83ca2-106">**UINT32**</span></span>

<span data-ttu-id="83ca2-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="83ca2-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ca2-108">備註</span><span class="sxs-lookup"><span data-stu-id="83ca2-108">Remarks</span></span>

<span data-ttu-id="83ca2-109">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="83ca2-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="83ca2-110">如果此值為 **TRUE**，表示檔案至少有一個影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="83ca2-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="83ca2-111">否則，檔案不會包含任何影片串流。</span><span class="sxs-lookup"><span data-stu-id="83ca2-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="83ca2-112">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="83ca2-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ca2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="83ca2-113">Requirements</span></span>



| <span data-ttu-id="83ca2-114">需求</span><span class="sxs-lookup"><span data-stu-id="83ca2-114">Requirement</span></span> | <span data-ttu-id="83ca2-115">值</span><span class="sxs-lookup"><span data-stu-id="83ca2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ca2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83ca2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="83ca2-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83ca2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83ca2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83ca2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="83ca2-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83ca2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83ca2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="83ca2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="83ca2-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="83ca2-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83ca2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83ca2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ca2-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="83ca2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="83ca2-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="83ca2-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="83ca2-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="83ca2-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="83ca2-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="83ca2-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="83ca2-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="83ca2-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="83ca2-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="83ca2-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




