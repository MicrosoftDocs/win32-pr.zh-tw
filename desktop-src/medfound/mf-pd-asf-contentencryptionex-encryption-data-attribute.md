---
description: 包含 Advanced 系統格式 (ASF) 檔的加密資料。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的擴充內容加密物件。
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: 'MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318800"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="bbd3a-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ 加密 \_ 資料屬性</span><span class="sxs-lookup"><span data-stu-id="bbd3a-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="bbd3a-105">包含 Advanced 系統格式 (ASF) 檔的加密資料。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="bbd3a-106">這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的擴充內容加密物件。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="bbd3a-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="bbd3a-107">Data type</span></span>

<span data-ttu-id="bbd3a-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="bbd3a-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd3a-109">備註</span><span class="sxs-lookup"><span data-stu-id="bbd3a-109">Remarks</span></span>

<span data-ttu-id="bbd3a-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="bbd3a-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從擴充內容加密物件標頭產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="bbd3a-112">Blob 的大小等於資料大小欄位。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="bbd3a-113">Blob 中包含的位元組陣列等於 ASF 標頭的擴充內容加密物件中的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="bbd3a-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd3a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd3a-114">Requirements</span></span>



| <span data-ttu-id="bbd3a-115">需求</span><span class="sxs-lookup"><span data-stu-id="bbd3a-115">Requirement</span></span> | <span data-ttu-id="bbd3a-116">值</span><span class="sxs-lookup"><span data-stu-id="bbd3a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd3a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbd3a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd3a-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd3a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bbd3a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbd3a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd3a-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd3a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bbd3a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bbd3a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd3a-122"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd3a-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd3a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbd3a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd3a-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bbd3a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbd3a-125">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="bbd3a-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="bbd3a-126">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="bbd3a-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="bbd3a-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bbd3a-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="bbd3a-128">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="bbd3a-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbd3a-129">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="bbd3a-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bbd3a-130">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="bbd3a-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




