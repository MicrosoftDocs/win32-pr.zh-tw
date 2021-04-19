---
description: 指定 Advanced 的系統格式 (ASF) 檔案是否使用 (VBR) 編碼的變數位元速率。
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: 'MF_PD_ASF_METADATA_IS_VBR 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983778"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="a5112-103">MF \_ PD \_ ASF \_ 中繼資料 \_ 是 \_ VBR 屬性</span><span class="sxs-lookup"><span data-stu-id="a5112-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="a5112-104">指定 Advanced 的系統格式 (ASF) 檔案是否使用 (VBR) 編碼的變數位元速率。</span><span class="sxs-lookup"><span data-stu-id="a5112-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5112-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a5112-105">Data type</span></span>

<span data-ttu-id="a5112-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5112-106">**UINT32**</span></span>

<span data-ttu-id="a5112-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="a5112-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5112-108">備註</span><span class="sxs-lookup"><span data-stu-id="a5112-108">Remarks</span></span>

<span data-ttu-id="a5112-109">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="a5112-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="a5112-110">如果值為 **TRUE**，則表示檔案是使用 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="a5112-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="a5112-111">如果值為 **FALSE** 或屬性不存在，則檔案不會使用 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="a5112-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="a5112-112">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，並在表示描述項上設定它。</span><span class="sxs-lookup"><span data-stu-id="a5112-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="a5112-113">這個屬性會對應至 Windows Media 格式 SDK 中的 **IsVBR** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a5112-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5112-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5112-114">Requirements</span></span>



| <span data-ttu-id="a5112-115">需求</span><span class="sxs-lookup"><span data-stu-id="a5112-115">Requirement</span></span> | <span data-ttu-id="a5112-116">值</span><span class="sxs-lookup"><span data-stu-id="a5112-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5112-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5112-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5112-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5112-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a5112-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5112-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5112-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5112-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5112-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a5112-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5112-122"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5112-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5112-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5112-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5112-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a5112-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5112-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5112-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a5112-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5112-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a5112-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a5112-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a5112-128">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="a5112-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5112-129">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="a5112-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a5112-130">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="a5112-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




