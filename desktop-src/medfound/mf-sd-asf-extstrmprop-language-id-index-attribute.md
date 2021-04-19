---
description: 以 Advanced Systems 格式 (ASF) 檔指定資料流程所使用的語言。
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: 'MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977985"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="59c61-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引屬性</span><span class="sxs-lookup"><span data-stu-id="59c61-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="59c61-104">以 Advanced Systems 格式 (ASF) 檔指定資料流程所使用的語言。</span><span class="sxs-lookup"><span data-stu-id="59c61-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="59c61-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="59c61-105">Data type</span></span>

<span data-ttu-id="59c61-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="59c61-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="59c61-107">備註</span><span class="sxs-lookup"><span data-stu-id="59c61-107">Remarks</span></span>

<span data-ttu-id="59c61-108">這個屬性會套用至 ASF 內容的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="59c61-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="59c61-109">值是包含在 [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) 屬性中的語言清單索引。</span><span class="sxs-lookup"><span data-stu-id="59c61-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="59c61-110">這個屬性會對應至擴充資料流程屬性物件中的資料流程語言識別項索引欄位。</span><span class="sxs-lookup"><span data-stu-id="59c61-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="59c61-111">如需詳細資訊，請參閱 ASF 規格。</span><span class="sxs-lookup"><span data-stu-id="59c61-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="59c61-112">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="59c61-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="59c61-113">應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)，從展示描述項建立資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="59c61-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="59c61-114">您也可以藉由查詢適用于 [**MF \_ SD \_ language**](mf-sd-language-attribute.md) 屬性的資料流程描述元來取得語言標記。</span><span class="sxs-lookup"><span data-stu-id="59c61-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c61-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="59c61-115">Requirements</span></span>



| <span data-ttu-id="59c61-116">需求</span><span class="sxs-lookup"><span data-stu-id="59c61-116">Requirement</span></span> | <span data-ttu-id="59c61-117">值</span><span class="sxs-lookup"><span data-stu-id="59c61-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c61-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59c61-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59c61-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59c61-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="59c61-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59c61-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59c61-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59c61-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59c61-122">標頭</span><span class="sxs-lookup"><span data-stu-id="59c61-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c61-123"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="59c61-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c61-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59c61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c61-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="59c61-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59c61-126">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59c61-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="59c61-127">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="59c61-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="59c61-128">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="59c61-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="59c61-129">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="59c61-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="59c61-130">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="59c61-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




