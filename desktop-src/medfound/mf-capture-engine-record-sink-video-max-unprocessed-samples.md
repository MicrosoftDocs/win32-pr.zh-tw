---
description: 設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: 'MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848529"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a><span data-ttu-id="8bb49-103">MF \_ CAPTURE \_ ENGINE \_ 記錄 \_ 接收 \_ 影片的 \_ 最大未處理 \_ \_ 樣本屬性</span><span class="sxs-lookup"><span data-stu-id="8bb49-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="8bb49-104">設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="8bb49-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="8bb49-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8bb49-105">Data type</span></span>

<span data-ttu-id="8bb49-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="8bb49-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb49-107">備註</span><span class="sxs-lookup"><span data-stu-id="8bb49-107">Remarks</span></span>

<span data-ttu-id="8bb49-108">若要在「捕獲引擎」上設定此屬性，請在呼叫 [**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)時，將它加入至 *pAttributes* 參數。</span><span class="sxs-lookup"><span data-stu-id="8bb49-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="8bb49-109">這個屬性的最大值為17。</span><span class="sxs-lookup"><span data-stu-id="8bb49-109">The maximum value for this attribute is 17.</span></span>

<span data-ttu-id="8bb49-110">一旦記錄已緩衝處理的樣本數目上限（由 MF \_ 捕捉 \_ 引擎 \_ 記錄接收影片的最大未處理範例所指定） \_ \_ \_ \_ \_ ，則會卸載範例以捨棄畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8bb49-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb49-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bb49-111">Requirements</span></span>



| <span data-ttu-id="8bb49-112">需求</span><span class="sxs-lookup"><span data-stu-id="8bb49-112">Requirement</span></span> | <span data-ttu-id="8bb49-113">值</span><span class="sxs-lookup"><span data-stu-id="8bb49-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb49-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bb49-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb49-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bb49-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8bb49-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bb49-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb49-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bb49-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8bb49-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8bb49-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb49-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb49-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb49-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bb49-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb49-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8bb49-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8bb49-122">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="8bb49-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="8bb49-123">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="8bb49-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




