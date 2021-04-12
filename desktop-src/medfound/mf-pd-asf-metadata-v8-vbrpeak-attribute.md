---
description: 以變動的位元速率指定最高的瞬間位元速率 (VBR) Advanced Systems 格式 (ASF) 檔。
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: 'MF_PD_ASF_METADATA_V8_VBRPEAK 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513693"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="20571-103">MF \_ PD \_ ASF \_ 中繼資料 \_ V8 \_ VBRPEAK 屬性</span><span class="sxs-lookup"><span data-stu-id="20571-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="20571-104">以變動的位元速率指定最高的瞬間位元速率 (VBR) Advanced Systems 格式 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="20571-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="20571-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="20571-105">Data type</span></span>

<span data-ttu-id="20571-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="20571-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="20571-107">備註</span><span class="sxs-lookup"><span data-stu-id="20571-107">Remarks</span></span>

<span data-ttu-id="20571-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="20571-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="20571-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="20571-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="20571-110">這個屬性只適用于 Windows Media Format SDK 第8版所建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="20571-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="20571-111">它會對應至 Windows Media 格式 SDK 中的 **VBRPeak** 屬性。</span><span class="sxs-lookup"><span data-stu-id="20571-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20571-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="20571-112">Requirements</span></span>



| <span data-ttu-id="20571-113">需求</span><span class="sxs-lookup"><span data-stu-id="20571-113">Requirement</span></span> | <span data-ttu-id="20571-114">值</span><span class="sxs-lookup"><span data-stu-id="20571-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20571-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20571-115">Minimum supported client</span></span><br/> | <span data-ttu-id="20571-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20571-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="20571-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20571-117">Minimum supported server</span></span><br/> | <span data-ttu-id="20571-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20571-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="20571-119">標頭</span><span class="sxs-lookup"><span data-stu-id="20571-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="20571-120"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="20571-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20571-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20571-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20571-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="20571-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="20571-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="20571-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="20571-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="20571-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="20571-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="20571-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="20571-126">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="20571-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="20571-127">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="20571-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="20571-128">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="20571-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




