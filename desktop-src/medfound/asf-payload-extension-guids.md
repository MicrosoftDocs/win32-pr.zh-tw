---
description: 下列 Guid 會定義 Advanced 系統格式 (ASF) 資料流程的承載延伸模組。
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: 'ASF 承載延伸模組 Guid (Wmcontainer .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510827"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="3d4be-103">ASF 承載延伸模組 Guid</span><span class="sxs-lookup"><span data-stu-id="3d4be-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="3d4be-104">下列 Guid 會定義 Advanced 系統格式 (ASF) 資料流程的承載延伸模組。</span><span class="sxs-lookup"><span data-stu-id="3d4be-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="3d4be-105">常數</span><span class="sxs-lookup"><span data-stu-id="3d4be-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="3d4be-106">描述</span><span class="sxs-lookup"><span data-stu-id="3d4be-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="3d4be-107"><dt>**MFASFSampleExtension \_ SampleDuration**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="3d4be-108">資料表示緩衝區物件中所含樣本的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d4be-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="3d4be-109"><dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="3d4be-110">資料會指出此範例是否為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="3d4be-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="3d4be-111">值為零表示此範例不是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="3d4be-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="3d4be-112">非零值表示它是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="3d4be-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="3d4be-113"><dt>**MFASFSampleExtension \_ SMPTE**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="3d4be-114">資料是 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="3d4be-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="3d4be-115"><dt>**MFASFSampleExtension \_ 檔案名**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="3d4be-116">範例延伸模組中的資料會指定從中取得範例內容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3d4be-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="3d4be-117"><dt>**MFASFSampleExtension \_ ContentType**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="3d4be-118">資料會識別此範例所包含的內容類型。</span><span class="sxs-lookup"><span data-stu-id="3d4be-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="3d4be-119"><dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="3d4be-120">資料會指出範例中內容的圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="3d4be-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="3d4be-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d4be-121">Requirements</span></span>



| <span data-ttu-id="3d4be-122">需求</span><span class="sxs-lookup"><span data-stu-id="3d4be-122">Requirement</span></span> | <span data-ttu-id="3d4be-123">值</span><span class="sxs-lookup"><span data-stu-id="3d4be-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4be-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d4be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4be-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d4be-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3d4be-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d4be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4be-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d4be-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d4be-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3d4be-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d4be-129"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4be-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d4be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4be-131">**IMFASFStreamConfig::AddPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="3d4be-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="3d4be-132">**IMFASFStreamConfig::GetPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="3d4be-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="3d4be-133">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="3d4be-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




