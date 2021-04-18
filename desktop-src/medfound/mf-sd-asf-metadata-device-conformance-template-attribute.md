---
description: 以 Advanced Systems 格式 (ASF) 檔，指定串流的裝置一致性範本。
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: 'MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983525"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="e6c75-103">MF \_ SD \_ ASF \_ 中繼資料 \_ 裝置 \_ 一致性 \_ 範本屬性</span><span class="sxs-lookup"><span data-stu-id="e6c75-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="e6c75-104">以 Advanced Systems 格式 (ASF) 檔，指定串流的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="e6c75-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="e6c75-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e6c75-105">Data type</span></span>

<span data-ttu-id="e6c75-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="e6c75-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c75-107">備註</span><span class="sxs-lookup"><span data-stu-id="e6c75-107">Remarks</span></span>

<span data-ttu-id="e6c75-108">這個屬性會套用至 ASF 內容的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="e6c75-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="e6c75-109">如需裝置一致性範本的詳細資訊，請參閱 Windows Media Format SDK 中的「裝置一致性範本參數」主題。</span><span class="sxs-lookup"><span data-stu-id="e6c75-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="e6c75-110">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e6c75-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c75-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6c75-111">Requirements</span></span>



| <span data-ttu-id="e6c75-112">需求</span><span class="sxs-lookup"><span data-stu-id="e6c75-112">Requirement</span></span> | <span data-ttu-id="e6c75-113">值</span><span class="sxs-lookup"><span data-stu-id="e6c75-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c75-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6c75-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c75-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6c75-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e6c75-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6c75-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c75-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6c75-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e6c75-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e6c75-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c75-119"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c75-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c75-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6c75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c75-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e6c75-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e6c75-122">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="e6c75-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="e6c75-123">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="e6c75-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="e6c75-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e6c75-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="e6c75-125">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="e6c75-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="e6c75-126">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="e6c75-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




