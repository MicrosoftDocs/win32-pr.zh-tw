---
description: 指定變數位元速率 (VBR) Advanced Systems 格式 (ASF) 檔所需的平均緩衝區大小。
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: 'MF_PD_ASF_METADATA_V8_BUFFERAVERAGE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972473"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="3a477-103">MF \_ PD \_ ASF \_ 中繼資料 \_ V8 \_ BUFFERAVERAGE 屬性</span><span class="sxs-lookup"><span data-stu-id="3a477-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="3a477-104">指定變數位元速率 (VBR) Advanced Systems 格式 (ASF) 檔所需的平均緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3a477-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a477-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3a477-105">Data type</span></span>

<span data-ttu-id="3a477-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a477-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a477-107">備註</span><span class="sxs-lookup"><span data-stu-id="3a477-107">Remarks</span></span>

<span data-ttu-id="3a477-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="3a477-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="3a477-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，此屬性會套用至 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="3a477-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="3a477-110">這個屬性只適用于 Windows Media Format SDK 第8版所建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="3a477-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="3a477-111">它會對應至 Windows Media 格式 SDK 中的 **BufferAverage** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3a477-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a477-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a477-112">Requirements</span></span>



| <span data-ttu-id="3a477-113">需求</span><span class="sxs-lookup"><span data-stu-id="3a477-113">Requirement</span></span> | <span data-ttu-id="3a477-114">值</span><span class="sxs-lookup"><span data-stu-id="3a477-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a477-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a477-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3a477-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a477-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a477-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a477-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3a477-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a477-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a477-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3a477-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a477-120"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a477-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a477-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a477-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a477-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3a477-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a477-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a477-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3a477-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a477-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3a477-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3a477-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3a477-126">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="3a477-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a477-127">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3a477-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="3a477-128">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="3a477-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




