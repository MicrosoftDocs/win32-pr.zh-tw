---
description: 指定加密 Advanced 系統格式 (ASF) 檔的金鑰識別碼。 這個屬性會對應至內容加密標頭的金鑰識別碼欄位，定義于 ASF 規格中。
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: 'MF_PD_ASF_CONTENTENCRYPTION_KEYID 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112888"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a><span data-ttu-id="e43e5-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID 屬性</span><span class="sxs-lookup"><span data-stu-id="e43e5-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_KEYID attribute</span></span>

<span data-ttu-id="e43e5-105">指定加密 Advanced 系統格式 (ASF) 檔的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="e43e5-105">Specifies the key identifier for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="e43e5-106">這個屬性會對應至內容加密標頭的金鑰識別碼欄位，定義于 ASF 規格中。</span><span class="sxs-lookup"><span data-stu-id="e43e5-106">This attribute corresponds to the Key ID field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="e43e5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e43e5-107">Data type</span></span>

<span data-ttu-id="e43e5-108">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="e43e5-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="e43e5-109">備註</span><span class="sxs-lookup"><span data-stu-id="e43e5-109">Remarks</span></span>

<span data-ttu-id="e43e5-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="e43e5-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="e43e5-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會抓取金鑰識別碼欄位、將它轉換為寬字元字串，然後填入以 null 終止的 **WCHAR** 陣列。</span><span class="sxs-lookup"><span data-stu-id="e43e5-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Key ID field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="e43e5-112">陣列的大小等於內容加密標頭的金鑰識別碼長度欄位。</span><span class="sxs-lookup"><span data-stu-id="e43e5-112">The size of the array equals the Key ID Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43e5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e43e5-113">Requirements</span></span>



| <span data-ttu-id="e43e5-114">需求</span><span class="sxs-lookup"><span data-stu-id="e43e5-114">Requirement</span></span> | <span data-ttu-id="e43e5-115">值</span><span class="sxs-lookup"><span data-stu-id="e43e5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e43e5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e43e5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e43e5-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e43e5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e43e5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e43e5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e43e5-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e43e5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e43e5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e43e5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e43e5-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="e43e5-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43e5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e43e5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43e5-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e43e5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e43e5-124">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="e43e5-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="e43e5-125">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="e43e5-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="e43e5-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e43e5-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="e43e5-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="e43e5-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="e43e5-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="e43e5-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="e43e5-129">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="e43e5-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




