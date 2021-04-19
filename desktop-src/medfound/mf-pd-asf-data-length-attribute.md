---
description: 以位元組為單位，指定 Advanced Systems 格式的 data 區段大小（以位元組為單位） (ASF) 檔。
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: 'MF_PD_ASF_DATA_LENGTH 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972446"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="5b388-103">MF \_ PD \_ ASF \_ 資料 \_ 長度屬性</span><span class="sxs-lookup"><span data-stu-id="5b388-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="5b388-104">以位元組為單位，指定 Advanced Systems 格式的 data 區段大小（以位元組為單位） (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="5b388-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b388-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5b388-105">Data type</span></span>

<span data-ttu-id="5b388-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5b388-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="5b388-107">備註</span><span class="sxs-lookup"><span data-stu-id="5b388-107">Remarks</span></span>

<span data-ttu-id="5b388-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="5b388-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="5b388-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5b388-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b388-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b388-110">Requirements</span></span>



| <span data-ttu-id="5b388-111">需求</span><span class="sxs-lookup"><span data-stu-id="5b388-111">Requirement</span></span> | <span data-ttu-id="5b388-112">值</span><span class="sxs-lookup"><span data-stu-id="5b388-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b388-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b388-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5b388-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b388-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b388-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b388-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5b388-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b388-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b388-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5b388-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b388-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b388-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b388-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b388-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b388-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5b388-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b388-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5b388-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5b388-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5b388-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="5b388-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5b388-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5b388-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="5b388-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b388-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="5b388-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




