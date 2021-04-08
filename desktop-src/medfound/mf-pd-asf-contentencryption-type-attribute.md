---
description: 指定用於 Advanced 系統格式 (ASF) 檔的保護機制類型。
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: 'MF_PD_ASF_CONTENTENCRYPTION_TYPE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847982"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="9524a-103">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE 屬性</span><span class="sxs-lookup"><span data-stu-id="9524a-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="9524a-104">指定用於 Advanced 系統格式 (ASF) 檔的保護機制類型。</span><span class="sxs-lookup"><span data-stu-id="9524a-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="9524a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9524a-105">Data type</span></span>

<span data-ttu-id="9524a-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="9524a-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="9524a-107">備註</span><span class="sxs-lookup"><span data-stu-id="9524a-107">Remarks</span></span>

<span data-ttu-id="9524a-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="9524a-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="9524a-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會抓取保護類型欄位、將其轉換為寬字元字串，然後填入以 null 終止的 **WCHAR** 陣列。</span><span class="sxs-lookup"><span data-stu-id="9524a-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="9524a-110">如果有的話，此值必須是「DRM」。</span><span class="sxs-lookup"><span data-stu-id="9524a-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="9524a-111">陣列的大小等於內容加密標頭的保護類型欄位長度欄位。</span><span class="sxs-lookup"><span data-stu-id="9524a-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="9524a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9524a-112">Requirements</span></span>



| <span data-ttu-id="9524a-113">需求</span><span class="sxs-lookup"><span data-stu-id="9524a-113">Requirement</span></span> | <span data-ttu-id="9524a-114">值</span><span class="sxs-lookup"><span data-stu-id="9524a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9524a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9524a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9524a-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9524a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9524a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9524a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9524a-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9524a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9524a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9524a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9524a-120"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="9524a-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9524a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9524a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9524a-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9524a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9524a-123">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="9524a-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="9524a-124">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="9524a-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="9524a-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9524a-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="9524a-126">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="9524a-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="9524a-127">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="9524a-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="9524a-128">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="9524a-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




