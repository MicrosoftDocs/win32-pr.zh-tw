---
description: 指定建立的 Advanced Systems 格式 (ASF) 檔的日期和時間。
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: 'MF_PD_ASF_FILEPROPERTIES_CREATION_TIME 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943398"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="a6db8-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="a6db8-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="a6db8-104">指定建立的 Advanced Systems 格式 (ASF) 檔的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a6db8-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6db8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a6db8-105">Data type</span></span>

<span data-ttu-id="a6db8-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="a6db8-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a6db8-107">備註</span><span class="sxs-lookup"><span data-stu-id="a6db8-107">Remarks</span></span>

<span data-ttu-id="a6db8-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="a6db8-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="a6db8-109">屬性的值是一個 **FILETIME** 結構，在 Windows SDK 中記載。</span><span class="sxs-lookup"><span data-stu-id="a6db8-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="a6db8-110">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a6db8-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6db8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6db8-111">Requirements</span></span>



| <span data-ttu-id="a6db8-112">需求</span><span class="sxs-lookup"><span data-stu-id="a6db8-112">Requirement</span></span> | <span data-ttu-id="a6db8-113">值</span><span class="sxs-lookup"><span data-stu-id="a6db8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6db8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6db8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a6db8-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6db8-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6db8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6db8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a6db8-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6db8-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6db8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a6db8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6db8-119"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6db8-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6db8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6db8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6db8-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a6db8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6db8-122">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a6db8-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a6db8-123">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a6db8-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a6db8-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a6db8-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a6db8-125">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="a6db8-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6db8-126">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="a6db8-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a6db8-127">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="a6db8-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




