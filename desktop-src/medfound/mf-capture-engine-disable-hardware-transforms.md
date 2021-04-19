---
description: 停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: 'MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983545"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="7ddd4-103">MF \_ 捕獲 \_ 引擎 \_ 停用 \_ 硬體 \_ 轉換屬性</span><span class="sxs-lookup"><span data-stu-id="7ddd4-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="7ddd4-104">停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。</span><span class="sxs-lookup"><span data-stu-id="7ddd4-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ddd4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7ddd4-105">Data type</span></span>

<span data-ttu-id="7ddd4-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7ddd4-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7ddd4-107">備註</span><span class="sxs-lookup"><span data-stu-id="7ddd4-107">Remarks</span></span>

<span data-ttu-id="7ddd4-108">根據預設，「捕獲引擎」會使用硬體解碼器或編碼器。</span><span class="sxs-lookup"><span data-stu-id="7ddd4-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="7ddd4-109">若要停用硬體 MFTs，請在建立 capture 引擎時將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7ddd4-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ddd4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ddd4-110">Requirements</span></span>



| <span data-ttu-id="7ddd4-111">需求</span><span class="sxs-lookup"><span data-stu-id="7ddd4-111">Requirement</span></span> | <span data-ttu-id="7ddd4-112">值</span><span class="sxs-lookup"><span data-stu-id="7ddd4-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddd4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ddd4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddd4-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ddd4-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7ddd4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ddd4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddd4-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ddd4-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ddd4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7ddd4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddd4-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddd4-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ddd4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ddd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddd4-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7ddd4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ddd4-121">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="7ddd4-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ddd4-122">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="7ddd4-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




