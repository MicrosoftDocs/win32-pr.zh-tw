---
description: 包含加密 Advanced 系統格式的機密資料 (ASF) 檔。 這個屬性會對應至內容加密標頭的秘密資料欄位，定義于 ASF 規格中。
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: 'MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511328"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="67468-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA 屬性</span><span class="sxs-lookup"><span data-stu-id="67468-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="67468-105">包含加密 Advanced 系統格式的機密資料 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="67468-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="67468-106">這個屬性會對應至內容加密標頭的秘密資料欄位，定義于 ASF 規格中。</span><span class="sxs-lookup"><span data-stu-id="67468-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="67468-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="67468-107">Data type</span></span>

<span data-ttu-id="67468-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="67468-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="67468-109">備註</span><span class="sxs-lookup"><span data-stu-id="67468-109">Remarks</span></span>

<span data-ttu-id="67468-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="67468-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="67468-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會在位元組陣列中填入 Secret 資料欄位。</span><span class="sxs-lookup"><span data-stu-id="67468-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="67468-112">陣列的大小等於內容加密標頭的秘密資料長度欄位。</span><span class="sxs-lookup"><span data-stu-id="67468-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="67468-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="67468-113">Requirements</span></span>



| <span data-ttu-id="67468-114">需求</span><span class="sxs-lookup"><span data-stu-id="67468-114">Requirement</span></span> | <span data-ttu-id="67468-115">值</span><span class="sxs-lookup"><span data-stu-id="67468-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67468-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67468-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67468-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67468-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="67468-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67468-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67468-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67468-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67468-120">標頭</span><span class="sxs-lookup"><span data-stu-id="67468-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67468-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="67468-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67468-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67468-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67468-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="67468-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67468-124">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="67468-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="67468-125">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="67468-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="67468-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="67468-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="67468-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="67468-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="67468-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="67468-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="67468-129">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="67468-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




