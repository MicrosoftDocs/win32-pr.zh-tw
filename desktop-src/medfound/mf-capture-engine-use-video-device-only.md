---
description: 指定捕捉引擎是否要捕獲影片，而非音訊。
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: 'MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943792"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="1d5a6-103">MF \_ 捕獲 \_ 引擎 \_ 使用 \_ \_ \_ 僅限影片裝置屬性</span><span class="sxs-lookup"><span data-stu-id="1d5a6-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="1d5a6-104">指定捕捉引擎是否要捕獲影片，而非音訊。</span><span class="sxs-lookup"><span data-stu-id="1d5a6-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d5a6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1d5a6-105">Data type</span></span>

<span data-ttu-id="1d5a6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1d5a6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d5a6-107">備註</span><span class="sxs-lookup"><span data-stu-id="1d5a6-107">Remarks</span></span>

<span data-ttu-id="1d5a6-108">如果此屬性為 **TRUE**，則表示捕獲引擎不會選取或使用音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="1d5a6-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="1d5a6-109">如果您想要在沒有音訊的情況下捕獲影片，請將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="1d5a6-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="1d5a6-110">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1d5a6-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5a6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d5a6-111">Requirements</span></span>



| <span data-ttu-id="1d5a6-112">需求</span><span class="sxs-lookup"><span data-stu-id="1d5a6-112">Requirement</span></span> | <span data-ttu-id="1d5a6-113">值</span><span class="sxs-lookup"><span data-stu-id="1d5a6-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5a6-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d5a6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5a6-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5a6-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1d5a6-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d5a6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5a6-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5a6-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1d5a6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1d5a6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d5a6-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d5a6-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5a6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d5a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5a6-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1d5a6-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d5a6-122">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="1d5a6-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d5a6-123">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="1d5a6-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




