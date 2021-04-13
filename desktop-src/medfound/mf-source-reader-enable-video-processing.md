---
description: 啟用來源讀取器的影片處理。
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: 'MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468989"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="900fe-103">MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理屬性</span><span class="sxs-lookup"><span data-stu-id="900fe-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="900fe-104">啟用 [來源讀取器](source-reader.md)的影片處理。</span><span class="sxs-lookup"><span data-stu-id="900fe-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="900fe-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="900fe-105">Data type</span></span>

<span data-ttu-id="900fe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="900fe-106">**UINT32**</span></span>



| <span data-ttu-id="900fe-107">值</span><span class="sxs-lookup"><span data-stu-id="900fe-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="900fe-108">意義</span><span class="sxs-lookup"><span data-stu-id="900fe-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="900fe-109"><dt>**零**</dt></span><span class="sxs-lookup"><span data-stu-id="900fe-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="900fe-110">啟用影片處理。</span><span class="sxs-lookup"><span data-stu-id="900fe-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="900fe-111"><dt>**零個**</dt></span><span class="sxs-lookup"><span data-stu-id="900fe-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="900fe-112">停用影片處理。</span><span class="sxs-lookup"><span data-stu-id="900fe-112">Disable video processing.</span></span> <span data-ttu-id="900fe-113">(預設值)</span><span class="sxs-lookup"><span data-stu-id="900fe-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="900fe-114">取得/設定</span><span class="sxs-lookup"><span data-stu-id="900fe-114">Get/set</span></span>

<span data-ttu-id="900fe-115">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="900fe-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="900fe-116">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="900fe-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="900fe-117">備註</span><span class="sxs-lookup"><span data-stu-id="900fe-117">Remarks</span></span>

<span data-ttu-id="900fe-118">如果此屬性為 **TRUE** (非零) ，來源讀取器可以在未壓縮的影片畫面上執行下列有限的影片處理：</span><span class="sxs-lookup"><span data-stu-id="900fe-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="900fe-119">從 YUV 轉換成 RGB-32。</span><span class="sxs-lookup"><span data-stu-id="900fe-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="900fe-120">去交錯.</span><span class="sxs-lookup"><span data-stu-id="900fe-120">Deinterlacing.</span></span>

<span data-ttu-id="900fe-121">這些作業是在軟體中執行，並不會針對播放進行優化。</span><span class="sxs-lookup"><span data-stu-id="900fe-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="900fe-122">這項功能適用于處理少量框架的應用程式（例如，建立影片縮圖），或是不會即時解碼框架的應用程式。</span><span class="sxs-lookup"><span data-stu-id="900fe-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="900fe-123">進行逐行壓縮作業時，會從單一欄位中插入資料，因此會有遺失的資料。</span><span class="sxs-lookup"><span data-stu-id="900fe-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="900fe-124">如果您使用 Direct3D 來顯示影片畫面，請避免此設定，因為 GPU 通常會提供更好的影片處理功能。</span><span class="sxs-lookup"><span data-stu-id="900fe-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="900fe-125">如果此屬性為 **TRUE**，則下列屬性必須為 **FALSE**：</span><span class="sxs-lookup"><span data-stu-id="900fe-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="900fe-126">MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="900fe-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="900fe-127">MF \_ READWRITE \_ 停用 \_ 轉換器</span><span class="sxs-lookup"><span data-stu-id="900fe-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="900fe-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="900fe-128">Requirements</span></span>



| <span data-ttu-id="900fe-129">需求</span><span class="sxs-lookup"><span data-stu-id="900fe-129">Requirement</span></span> | <span data-ttu-id="900fe-130">值</span><span class="sxs-lookup"><span data-stu-id="900fe-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="900fe-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="900fe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="900fe-132">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900fe-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="900fe-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="900fe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="900fe-134">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="900fe-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="900fe-135">標頭</span><span class="sxs-lookup"><span data-stu-id="900fe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="900fe-136"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="900fe-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="900fe-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="900fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900fe-138">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="900fe-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="900fe-139">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="900fe-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="900fe-140">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="900fe-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




