---
description: 指定 Advanced 系統格式的檔案識別碼 (ASF) 檔。
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: 'MF_PD_ASF_FILEPROPERTIES_FILE_ID 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969266"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="16f7d-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 檔案 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="16f7d-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="16f7d-104">指定 Advanced 系統格式的檔案識別碼 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="16f7d-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="16f7d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="16f7d-105">Data type</span></span>

<span data-ttu-id="16f7d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="16f7d-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="16f7d-107">備註</span><span class="sxs-lookup"><span data-stu-id="16f7d-107">Remarks</span></span>

<span data-ttu-id="16f7d-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="16f7d-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="16f7d-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="16f7d-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f7d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="16f7d-110">Requirements</span></span>



| <span data-ttu-id="16f7d-111">需求</span><span class="sxs-lookup"><span data-stu-id="16f7d-111">Requirement</span></span> | <span data-ttu-id="16f7d-112">值</span><span class="sxs-lookup"><span data-stu-id="16f7d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f7d-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16f7d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="16f7d-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16f7d-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16f7d-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16f7d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="16f7d-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16f7d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16f7d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="16f7d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="16f7d-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="16f7d-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f7d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16f7d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f7d-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="16f7d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="16f7d-121">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="16f7d-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="16f7d-122">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="16f7d-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="16f7d-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="16f7d-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="16f7d-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="16f7d-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="16f7d-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="16f7d-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="16f7d-126">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="16f7d-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




