---
description: 以 Advanced Systems 格式的資料流程指定平均位元速率（以每秒位數為單位）， (ASF) 檔。 這個屬性會對應至在 ASF 規格中定義的資料流程位元速率屬性物件。
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: 'MF_SD_ASF_STREAMBITRATES_BITRATE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984204"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="a9b7c-104">MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率屬性</span><span class="sxs-lookup"><span data-stu-id="a9b7c-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="a9b7c-105">以 Advanced Systems 格式的資料流程指定平均位元速率（以每秒位數為單位）， (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="a9b7c-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a9b7c-106">這個屬性會對應至在 ASF 規格中定義的資料流程位元速率屬性物件。</span><span class="sxs-lookup"><span data-stu-id="a9b7c-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="a9b7c-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a9b7c-107">Data type</span></span>

<span data-ttu-id="a9b7c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b7c-109">備註</span><span class="sxs-lookup"><span data-stu-id="a9b7c-109">Remarks</span></span>

<span data-ttu-id="a9b7c-110">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，並在資料流程描述項上設定它。</span><span class="sxs-lookup"><span data-stu-id="a9b7c-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="a9b7c-111">應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)，從展示描述項建立資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="a9b7c-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="a9b7c-112">屬性值等於資料流程位速率屬性物件中的平均位元速率欄位。</span><span class="sxs-lookup"><span data-stu-id="a9b7c-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b7c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9b7c-113">Requirements</span></span>



| <span data-ttu-id="a9b7c-114">需求</span><span class="sxs-lookup"><span data-stu-id="a9b7c-114">Requirement</span></span> | <span data-ttu-id="a9b7c-115">值</span><span class="sxs-lookup"><span data-stu-id="a9b7c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b7c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9b7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b7c-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9b7c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9b7c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9b7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b7c-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9b7c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9b7c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a9b7c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b7c-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b7c-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b7c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9b7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b7c-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a9b7c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9b7c-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a9b7c-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a9b7c-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a9b7c-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="a9b7c-127">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="a9b7c-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9b7c-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="a9b7c-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




