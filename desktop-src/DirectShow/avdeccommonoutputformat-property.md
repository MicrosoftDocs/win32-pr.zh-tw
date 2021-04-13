---
description: 指定此解碼器的輸出格式。
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: 'AVDecCommonOutputFormat 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510281"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="982ec-103">AVDecCommonOutputFormat 屬性</span><span class="sxs-lookup"><span data-stu-id="982ec-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="982ec-104">指定此解碼器的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="982ec-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="982ec-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="982ec-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="982ec-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="982ec-106">Data type</span></span>

<span data-ttu-id="982ec-107">**BSTR** (**VT \_ bstr**) </span><span class="sxs-lookup"><span data-stu-id="982ec-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="982ec-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="982ec-108">Property GUID</span></span>

<span data-ttu-id="982ec-109">**CODECAPI \_ AVDecCommonOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="982ec-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="982ec-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="982ec-110">Property value</span></span>



| <span data-ttu-id="982ec-111">GUID</span><span class="sxs-lookup"><span data-stu-id="982ec-111">GUID</span></span>                                                               | <span data-ttu-id="982ec-112">Description</span><span class="sxs-lookup"><span data-stu-id="982ec-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="982ec-113">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM</span><span class="sxs-lookup"><span data-stu-id="982ec-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="982ec-114">PCM 音訊，使用任意數目的頻道</span><span class="sxs-lookup"><span data-stu-id="982ec-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="982ec-115">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 耳機</span><span class="sxs-lookup"><span data-stu-id="982ec-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="982ec-116">身歷聲 PCM 音訊，使用僅限左/右 (Lo/Ro) downmix</span><span class="sxs-lookup"><span data-stu-id="982ec-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="982ec-117">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 身歷聲 \_ 自動</span><span class="sxs-lookup"><span data-stu-id="982ec-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="982ec-118">身歷聲 PCM 音訊，使用自動選取的身歷聲 downmix 模式 (Lo/Ro 或 Lt/Rt) 。</span><span class="sxs-lookup"><span data-stu-id="982ec-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="982ec-119">您可以將此值用於輸入資料流程定義慣用 downmix 模式的音訊格式，例如 [杜比 AC-3]。</span><span class="sxs-lookup"><span data-stu-id="982ec-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="982ec-120">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ 身歷聲 \_ MatrixEncoded</span><span class="sxs-lookup"><span data-stu-id="982ec-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="982ec-121">身歷聲 PCM 音訊，使用矩陣編碼的身歷聲 downmix (Lt/Rt) </span><span class="sxs-lookup"><span data-stu-id="982ec-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="982ec-122">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ 位流</span><span class="sxs-lookup"><span data-stu-id="982ec-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="982ec-123">S/PDIF (索尼/Philips 數位介面格式) 壓縮位流，如 IEC-60958 所定義</span><span class="sxs-lookup"><span data-stu-id="982ec-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="982ec-124">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="982ec-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="982ec-125">S/PDIF PCM 身歷聲，如 IEC-60958 所定義</span><span class="sxs-lookup"><span data-stu-id="982ec-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="982ec-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="982ec-126">Requirements</span></span>



| <span data-ttu-id="982ec-127">需求</span><span class="sxs-lookup"><span data-stu-id="982ec-127">Requirement</span></span> | <span data-ttu-id="982ec-128">值</span><span class="sxs-lookup"><span data-stu-id="982ec-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="982ec-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="982ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="982ec-130">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="982ec-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="982ec-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="982ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="982ec-132">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="982ec-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="982ec-133">標頭</span><span class="sxs-lookup"><span data-stu-id="982ec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="982ec-134"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="982ec-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="982ec-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="982ec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="982ec-136">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="982ec-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="982ec-137">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="982ec-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




