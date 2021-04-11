---
description: 在 capture 引擎上設定 DXGI 裝置管理員的指標。
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: 'MF_CAPTURE_ENGINE_D3D_MANAGER 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113684"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="d7f5c-103">MF \_ CAPTURE \_ ENGINE \_ D3D \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="d7f5c-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="d7f5c-104">在 capture 引擎上設定 DXGI 裝置管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="d7f5c-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7f5c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d7f5c-105">Data type</span></span>

<span data-ttu-id="d7f5c-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="d7f5c-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f5c-107">備註</span><span class="sxs-lookup"><span data-stu-id="d7f5c-107">Remarks</span></span>

<span data-ttu-id="d7f5c-108">這個屬性的值是 [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d7f5c-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="d7f5c-109">此屬性可讓 capture engine 使用 DXGI 介面配置影片框架，並使用硬體加速進行解碼和影片處理。</span><span class="sxs-lookup"><span data-stu-id="d7f5c-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f5c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7f5c-110">Requirements</span></span>



| <span data-ttu-id="d7f5c-111">需求</span><span class="sxs-lookup"><span data-stu-id="d7f5c-111">Requirement</span></span> | <span data-ttu-id="d7f5c-112">值</span><span class="sxs-lookup"><span data-stu-id="d7f5c-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f5c-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7f5c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f5c-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7f5c-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d7f5c-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7f5c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f5c-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7f5c-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7f5c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d7f5c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f5c-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f5c-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f5c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7f5c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f5c-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d7f5c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7f5c-121">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="d7f5c-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7f5c-122">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="d7f5c-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




