---
description: 指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: 'MFASFSPLITTER_PACKET_BOUNDARY 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997096"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="15ba1-103">MFASFSPLITTER 封 \_ 包 \_ 界限屬性</span><span class="sxs-lookup"><span data-stu-id="15ba1-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="15ba1-104">指定緩衝區是否包含 Advanced 系統格式的開頭 (ASF) 封包。</span><span class="sxs-lookup"><span data-stu-id="15ba1-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="15ba1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="15ba1-105">Data type</span></span>

<span data-ttu-id="15ba1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="15ba1-106">**UINT32**</span></span>

<span data-ttu-id="15ba1-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="15ba1-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ba1-108">備註</span><span class="sxs-lookup"><span data-stu-id="15ba1-108">Remarks</span></span>

<span data-ttu-id="15ba1-109">如果媒體緩衝區透過 **QueryInterface** 公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面，且這個屬性的值為非零值，則 ASF 分隔器會將緩衝區視為新封包的開頭。</span><span class="sxs-lookup"><span data-stu-id="15ba1-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="15ba1-110">如果您使用 ASF 分隔器來剖析 ASF 資料，則會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="15ba1-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="15ba1-111">如果您的 ASF 資料具有可變的封包長度，您必須在傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法的媒體緩衝區上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="15ba1-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="15ba1-112">如果緩衝區包含新封包的開頭，請將屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="15ba1-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="15ba1-113">如果緩衝區包含前一個封包的接續，請將屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="15ba1-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="15ba1-114">緩衝區無法跨越多個封包。</span><span class="sxs-lookup"><span data-stu-id="15ba1-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="15ba1-115">若為具有固定封包大小的 ASF 資料，則不需要此屬性，而且緩衝區可以橫跨多個封包。</span><span class="sxs-lookup"><span data-stu-id="15ba1-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="15ba1-116">請注意，媒體基礎提供的標準 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 不會公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。</span><span class="sxs-lookup"><span data-stu-id="15ba1-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="15ba1-117">若要使用此屬性，您必須提供您自己的 **IMFMediaBuffer** 實值;例如，藉由包裝 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer)所傳回的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="15ba1-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="15ba1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="15ba1-118">Requirements</span></span>



| <span data-ttu-id="15ba1-119">需求</span><span class="sxs-lookup"><span data-stu-id="15ba1-119">Requirement</span></span> | <span data-ttu-id="15ba1-120">值</span><span class="sxs-lookup"><span data-stu-id="15ba1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ba1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15ba1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15ba1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ba1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="15ba1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15ba1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15ba1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ba1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15ba1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="15ba1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ba1-126"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="15ba1-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ba1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15ba1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ba1-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="15ba1-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15ba1-129">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="15ba1-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="15ba1-130">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="15ba1-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="15ba1-131">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="15ba1-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="15ba1-132">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="15ba1-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




