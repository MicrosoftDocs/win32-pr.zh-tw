---
description: 指定 Advanced Systems 格式之 data 區段中的封包數目 (ASF) 檔。
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: 'MF_PD_ASF_FILEPROPERTIES_PACKETS 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943397"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="04393-103">MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包屬性</span><span class="sxs-lookup"><span data-stu-id="04393-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="04393-104">指定 Advanced Systems 格式之 data 區段中的封包數目 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="04393-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="04393-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="04393-105">Data type</span></span>

<span data-ttu-id="04393-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="04393-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="04393-107">備註</span><span class="sxs-lookup"><span data-stu-id="04393-107">Remarks</span></span>

<span data-ttu-id="04393-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="04393-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="04393-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="04393-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="04393-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="04393-110">Requirements</span></span>



| <span data-ttu-id="04393-111">需求</span><span class="sxs-lookup"><span data-stu-id="04393-111">Requirement</span></span> | <span data-ttu-id="04393-112">值</span><span class="sxs-lookup"><span data-stu-id="04393-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04393-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04393-113">Minimum supported client</span></span><br/> | <span data-ttu-id="04393-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04393-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04393-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04393-115">Minimum supported server</span></span><br/> | <span data-ttu-id="04393-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04393-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04393-117">標頭</span><span class="sxs-lookup"><span data-stu-id="04393-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="04393-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="04393-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04393-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04393-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04393-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="04393-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04393-121">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="04393-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="04393-122">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="04393-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="04393-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="04393-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="04393-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="04393-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="04393-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="04393-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="04393-126">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="04393-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




