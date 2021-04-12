---
description: 指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: 'MF_CAPTURE_ENGINE_DISABLE_DXVA 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318551"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="81cbb-103">MF \_ 捕獲 \_ 引擎 \_ 停用 \_ DXVA 屬性</span><span class="sxs-lookup"><span data-stu-id="81cbb-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="81cbb-104">指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。</span><span class="sxs-lookup"><span data-stu-id="81cbb-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="81cbb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="81cbb-105">Data type</span></span>

<span data-ttu-id="81cbb-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="81cbb-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="81cbb-107">備註</span><span class="sxs-lookup"><span data-stu-id="81cbb-107">Remarks</span></span>

<span data-ttu-id="81cbb-108">如果下列條件成立，則適用此屬性：</span><span class="sxs-lookup"><span data-stu-id="81cbb-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="81cbb-109">捕獲引擎會從捕獲裝置解碼壓縮的影片串流 (例如，如果捕捉裝置輸出 h.264 video) 。</span><span class="sxs-lookup"><span data-stu-id="81cbb-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="81cbb-110">影片解碼支援使用 DXVA 進行硬體加速解碼。</span><span class="sxs-lookup"><span data-stu-id="81cbb-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="81cbb-111">應用程式會使用「 [MF \_ 捕捉引擎」 \_ \_ D3D \_ 管理員](mf-capture-engine-d3d-manager.md) 屬性，在「捕獲引擎」上設定 DXGI 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="81cbb-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="81cbb-112">否則，會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="81cbb-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="81cbb-113">這個屬性可讓應用程式停用 DXVA，同時仍在對 Direct3D 介面進行解碼。</span><span class="sxs-lookup"><span data-stu-id="81cbb-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="81cbb-114">這個屬性的預設值為 **FALSE**，表示 DXVA 解碼會在可用時啟用。</span><span class="sxs-lookup"><span data-stu-id="81cbb-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="81cbb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="81cbb-115">Requirements</span></span>



| <span data-ttu-id="81cbb-116">需求</span><span class="sxs-lookup"><span data-stu-id="81cbb-116">Requirement</span></span> | <span data-ttu-id="81cbb-117">值</span><span class="sxs-lookup"><span data-stu-id="81cbb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="81cbb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81cbb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="81cbb-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81cbb-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="81cbb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81cbb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="81cbb-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81cbb-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="81cbb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="81cbb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="81cbb-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="81cbb-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81cbb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81cbb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81cbb-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="81cbb-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81cbb-126">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="81cbb-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="81cbb-127">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="81cbb-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




