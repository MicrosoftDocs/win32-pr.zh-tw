---
description: 指定 Advanced 系統格式 (ASF) 檔的最大瞬間位元速率（以每秒位數為單位）。
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: 'MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849219"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="bb8e9-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最大 \_ 位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="bb8e9-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="bb8e9-104">指定 Advanced 系統格式 (ASF) 檔的最大瞬間位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb8e9-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb8e9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bb8e9-105">Data type</span></span>

<span data-ttu-id="bb8e9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bb8e9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bb8e9-107">備註</span><span class="sxs-lookup"><span data-stu-id="bb8e9-107">Remarks</span></span>

<span data-ttu-id="bb8e9-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="bb8e9-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="bb8e9-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bb8e9-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb8e9-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb8e9-110">Requirements</span></span>



| <span data-ttu-id="bb8e9-111">需求</span><span class="sxs-lookup"><span data-stu-id="bb8e9-111">Requirement</span></span> | <span data-ttu-id="bb8e9-112">值</span><span class="sxs-lookup"><span data-stu-id="bb8e9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8e9-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb8e9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8e9-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb8e9-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bb8e9-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb8e9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8e9-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb8e9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bb8e9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="bb8e9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb8e9-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8e9-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb8e9-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb8e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8e9-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bb8e9-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb8e9-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb8e9-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bb8e9-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb8e9-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bb8e9-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bb8e9-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="bb8e9-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="bb8e9-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb8e9-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="bb8e9-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bb8e9-126">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="bb8e9-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




