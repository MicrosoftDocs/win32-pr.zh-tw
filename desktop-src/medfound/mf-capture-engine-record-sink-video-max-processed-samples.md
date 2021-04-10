---
description: 設定可在記錄接收影片路徑中緩衝處理之已處理樣本的最大數目。
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: 'MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690904"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="23038-103">MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 影片的 \_ 最大 \_ 處理 \_ 樣本屬性</span><span class="sxs-lookup"><span data-stu-id="23038-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="23038-104">設定可在記錄接收影片路徑中緩衝處理之已處理樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="23038-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="23038-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="23038-105">Data type</span></span>

<span data-ttu-id="23038-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="23038-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="23038-107">備註</span><span class="sxs-lookup"><span data-stu-id="23038-107">Remarks</span></span>

<span data-ttu-id="23038-108">若要在「捕獲引擎」上設定此屬性，請在呼叫 [**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)時，將它加入至 *pAttributes* 參數。</span><span class="sxs-lookup"><span data-stu-id="23038-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="23038-109">這個屬性的最大值為17。</span><span class="sxs-lookup"><span data-stu-id="23038-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="23038-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="23038-110">Requirements</span></span>



| <span data-ttu-id="23038-111">需求</span><span class="sxs-lookup"><span data-stu-id="23038-111">Requirement</span></span> | <span data-ttu-id="23038-112">值</span><span class="sxs-lookup"><span data-stu-id="23038-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23038-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23038-113">Minimum supported client</span></span><br/> | <span data-ttu-id="23038-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23038-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="23038-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23038-115">Minimum supported server</span></span><br/> | <span data-ttu-id="23038-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23038-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23038-117">標頭</span><span class="sxs-lookup"><span data-stu-id="23038-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="23038-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="23038-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23038-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23038-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23038-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="23038-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="23038-121">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="23038-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="23038-122">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="23038-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




