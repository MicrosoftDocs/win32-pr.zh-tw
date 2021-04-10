---
description: 包含 [3GP] 檔案的 [範例描述] 方塊。
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: 'MF_MT_MPEG4_SAMPLE_DESCRIPTION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851428"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="ce775-103">MF \_ MT \_ MPEG4 \_ 範例 \_ DESCRIPTION 屬性</span><span class="sxs-lookup"><span data-stu-id="ce775-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="ce775-104">包含 [3GP] 檔案的 [範例描述] 方塊。</span><span class="sxs-lookup"><span data-stu-id="ce775-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce775-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ce775-105">Data type</span></span>

<span data-ttu-id="ce775-106">**位元組\[\]**</span><span class="sxs-lookup"><span data-stu-id="ce775-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="ce775-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="ce775-107">Get/set</span></span>

<span data-ttu-id="ce775-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="ce775-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="ce775-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="ce775-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce775-110">適用於</span><span class="sxs-lookup"><span data-stu-id="ce775-110">Applies to</span></span>

[<span data-ttu-id="ce775-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ce775-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="ce775-112">備註</span><span class="sxs-lookup"><span data-stu-id="ce775-112">Remarks</span></span>

<span data-ttu-id="ce775-113">[範例描述] 方塊描述檔案中資料流程所使用的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="ce775-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="ce775-114">MPEG 4 檔案來源會在每個資料流程的媒體類型上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ce775-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="ce775-115">屬性的值是 [範例描述] 方塊中的原始資料。</span><span class="sxs-lookup"><span data-stu-id="ce775-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="ce775-116">如果 MPEG 檔來源可以剖析範例描述，也會將格式詳細資料新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ce775-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="ce775-117">否則，應用程式或解碼器必須剖析來自 MF \_ MT \_ MPEG4 \_ 範例 \_ description 屬性的範例描述。</span><span class="sxs-lookup"><span data-stu-id="ce775-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="ce775-118">當您透過 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 方法在 MPEG 4 上設定此屬性時，如果 \_ 已將 \_ \_ \_ 一或多個範例傳送至對應資料流程的 [**IMFStreamSink：:P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) 介面上的接收，則不應變更屬性 MF MT MPEG4 範例描述的資料。</span><span class="sxs-lookup"><span data-stu-id="ce775-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="ce775-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ce775-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce775-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce775-120">Requirements</span></span>



| <span data-ttu-id="ce775-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce775-121">Requirement</span></span> | <span data-ttu-id="ce775-122">值</span><span class="sxs-lookup"><span data-stu-id="ce775-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce775-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce775-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce775-124">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce775-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ce775-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce775-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce775-126">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce775-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ce775-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ce775-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce775-128"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce775-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce775-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce775-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce775-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ce775-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce775-131">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="ce775-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




