---
description: 指定加密 Advanced 系統格式的授權取得 URL (ASF) 檔。 這個屬性會對應至內容加密標頭的 [授權 URL] 欄位，定義于 ASF 規格中。
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: 'MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468996"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a><span data-ttu-id="eeff6-104">MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 授權 \_ URL 屬性</span><span class="sxs-lookup"><span data-stu-id="eeff6-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_LICENSE\_URL attribute</span></span>

<span data-ttu-id="eeff6-105">指定加密 Advanced 系統格式的授權取得 URL (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="eeff6-105">Specifies the license acquisition URL for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="eeff6-106">這個屬性會對應至內容加密標頭的 [授權 URL] 欄位，定義于 ASF 規格中。</span><span class="sxs-lookup"><span data-stu-id="eeff6-106">This attribute corresponds to the License URL field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="eeff6-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="eeff6-107">Data type</span></span>

<span data-ttu-id="eeff6-108">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="eeff6-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="eeff6-109">備註</span><span class="sxs-lookup"><span data-stu-id="eeff6-109">Remarks</span></span>

<span data-ttu-id="eeff6-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="eeff6-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="eeff6-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會抓取授權 URL 欄位、將其轉換為寬字元字串，然後填入以 null 終止的 **WCHAR** 陣列。</span><span class="sxs-lookup"><span data-stu-id="eeff6-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the License URL field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="eeff6-112">陣列的大小等於內容加密標頭的授權 URL 長度欄位。</span><span class="sxs-lookup"><span data-stu-id="eeff6-112">The size of the array equals the License URL Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeff6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeff6-113">Requirements</span></span>



| <span data-ttu-id="eeff6-114">需求</span><span class="sxs-lookup"><span data-stu-id="eeff6-114">Requirement</span></span> | <span data-ttu-id="eeff6-115">值</span><span class="sxs-lookup"><span data-stu-id="eeff6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeff6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeff6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eeff6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeff6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eeff6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeff6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eeff6-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeff6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eeff6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="eeff6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeff6-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeff6-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeff6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeff6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeff6-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="eeff6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eeff6-124">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="eeff6-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="eeff6-125">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="eeff6-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="eeff6-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="eeff6-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="eeff6-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="eeff6-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="eeff6-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="eeff6-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="eeff6-129">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="eeff6-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




