---
description: 以位元組為單位，指定 Advanced 系統格式 (ASF) 檔的最小封包大小。
ms.assetid: 8c62db36-1332-4565-9fc0-885b9fc148e1
title: 'MF_PD_ASF_FILEPROPERTIES_MIN_PACKET_SIZE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e7b9016184096696ffd74cde6bd51f305778e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980963"
---
# <a name="mf_pd_asf_fileproperties_min_packet_size-attribute"></a><span data-ttu-id="3d514-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="3d514-103">MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="3d514-104">以位元組為單位，指定 Advanced 系統格式 (ASF) 檔的最小封包大小。</span><span class="sxs-lookup"><span data-stu-id="3d514-104">Specifies the minimum packet size, in bytes, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d514-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3d514-105">Data type</span></span>

<span data-ttu-id="3d514-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3d514-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d514-107">備註</span><span class="sxs-lookup"><span data-stu-id="3d514-107">Remarks</span></span>

<span data-ttu-id="3d514-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="3d514-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="3d514-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3d514-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d514-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d514-110">Requirements</span></span>



| <span data-ttu-id="3d514-111">需求</span><span class="sxs-lookup"><span data-stu-id="3d514-111">Requirement</span></span> | <span data-ttu-id="3d514-112">值</span><span class="sxs-lookup"><span data-stu-id="3d514-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d514-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d514-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3d514-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d514-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3d514-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d514-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3d514-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d514-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d514-117">標頭</span><span class="sxs-lookup"><span data-stu-id="3d514-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d514-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d514-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d514-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d514-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d514-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3d514-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d514-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3d514-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3d514-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3d514-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3d514-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3d514-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3d514-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="3d514-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d514-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3d514-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="3d514-126">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="3d514-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




