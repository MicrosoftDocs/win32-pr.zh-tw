---
description: 以位元組為單位，指定 Advanced Systems 格式的資料流程所需的平均緩衝區大小 (ASF) 檔。
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: 'MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850068"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="3910c-103">MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="3910c-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="3910c-104">以位元組為單位，指定 Advanced Systems 格式的資料流程所需的平均緩衝區大小 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="3910c-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="3910c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3910c-105">Data type</span></span>

<span data-ttu-id="3910c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3910c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3910c-107">備註</span><span class="sxs-lookup"><span data-stu-id="3910c-107">Remarks</span></span>

<span data-ttu-id="3910c-108">這個屬性會套用至 ASF 內容的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="3910c-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="3910c-109">它會對應至擴充資料流程屬性物件中的 [緩衝區大小] 欄位，並定義「有漏洞 bucket」模型中所使用的值區大小。</span><span class="sxs-lookup"><span data-stu-id="3910c-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="3910c-110">如需詳細資訊，請參閱 ASF 規格。</span><span class="sxs-lookup"><span data-stu-id="3910c-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="3910c-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3910c-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="3910c-112">應用程式可以藉由呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)，從展示描述項建立資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="3910c-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="3910c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3910c-113">Requirements</span></span>



| <span data-ttu-id="3910c-114">需求</span><span class="sxs-lookup"><span data-stu-id="3910c-114">Requirement</span></span> | <span data-ttu-id="3910c-115">值</span><span class="sxs-lookup"><span data-stu-id="3910c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3910c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3910c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3910c-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3910c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3910c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3910c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3910c-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3910c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3910c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3910c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3910c-121"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="3910c-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3910c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3910c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3910c-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3910c-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3910c-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3910c-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3910c-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3910c-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3910c-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3910c-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="3910c-127">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="3910c-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3910c-128">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="3910c-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




