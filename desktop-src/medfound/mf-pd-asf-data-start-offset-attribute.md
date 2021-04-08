---
description: 指定從 Advanced 系統格式開頭的位移（以位元組為單位） (ASF) 檔到第一個資料封包的開頭。
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: 'MF_PD_ASF_DATA_START_OFFSET 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851424"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="59ee8-103">MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移屬性</span><span class="sxs-lookup"><span data-stu-id="59ee8-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="59ee8-104">指定從 Advanced 系統格式開頭的位移（以位元組為單位） (ASF) 檔到第一個資料封包的開頭。</span><span class="sxs-lookup"><span data-stu-id="59ee8-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="59ee8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="59ee8-105">Data type</span></span>

<span data-ttu-id="59ee8-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="59ee8-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="59ee8-107">備註</span><span class="sxs-lookup"><span data-stu-id="59ee8-107">Remarks</span></span>

<span data-ttu-id="59ee8-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="59ee8-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="59ee8-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="59ee8-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ee8-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="59ee8-110">Requirements</span></span>



| <span data-ttu-id="59ee8-111">需求</span><span class="sxs-lookup"><span data-stu-id="59ee8-111">Requirement</span></span> | <span data-ttu-id="59ee8-112">值</span><span class="sxs-lookup"><span data-stu-id="59ee8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ee8-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59ee8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="59ee8-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59ee8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="59ee8-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59ee8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="59ee8-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59ee8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59ee8-117">標頭</span><span class="sxs-lookup"><span data-stu-id="59ee8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ee8-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="59ee8-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ee8-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59ee8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ee8-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="59ee8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59ee8-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="59ee8-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="59ee8-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="59ee8-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="59ee8-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="59ee8-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="59ee8-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="59ee8-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="59ee8-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="59ee8-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




