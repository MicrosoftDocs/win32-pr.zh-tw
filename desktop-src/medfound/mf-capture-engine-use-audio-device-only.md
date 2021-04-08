---
description: 指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: 'MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943546"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="cf641-103">MF \_ 捕獲 \_ 引擎 \_ 使用 \_ \_ \_ 僅限音訊裝置屬性</span><span class="sxs-lookup"><span data-stu-id="cf641-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="cf641-104">指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。</span><span class="sxs-lookup"><span data-stu-id="cf641-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf641-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cf641-105">Data type</span></span>

<span data-ttu-id="cf641-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cf641-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cf641-107">備註</span><span class="sxs-lookup"><span data-stu-id="cf641-107">Remarks</span></span>

<span data-ttu-id="cf641-108">如果此屬性為 **TRUE**，則表示捕獲引擎不會選取或使用影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="cf641-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="cf641-109">如果您想要在沒有影片的情況下捕獲音訊，請將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cf641-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="cf641-110">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cf641-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf641-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf641-111">Requirements</span></span>



| <span data-ttu-id="cf641-112">需求</span><span class="sxs-lookup"><span data-stu-id="cf641-112">Requirement</span></span> | <span data-ttu-id="cf641-113">值</span><span class="sxs-lookup"><span data-stu-id="cf641-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf641-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf641-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cf641-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf641-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="cf641-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf641-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cf641-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf641-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf641-118">標頭</span><span class="sxs-lookup"><span data-stu-id="cf641-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf641-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf641-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf641-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf641-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf641-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cf641-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf641-122">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="cf641-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf641-123">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="cf641-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




