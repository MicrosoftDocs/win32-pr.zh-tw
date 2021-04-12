---
description: 表示已在捕獲引擎上設定輸出類型，以回應 IMFCaptureSink2：： SetOutputType。
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: 'MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321635"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a><span data-ttu-id="09180-103">MF \_ CAPTURE \_ ENGINE \_ 輸出 \_ 媒體 \_ 類型 \_ 設定屬性</span><span class="sxs-lookup"><span data-stu-id="09180-103">MF\_CAPTURE\_ENGINE\_OUTPUT\_MEDIA\_TYPE\_SET attribute</span></span>

<span data-ttu-id="09180-104">表示已在捕獲引擎上設定輸出類型，以回應 [**IMFCaptureSink2：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。</span><span class="sxs-lookup"><span data-stu-id="09180-104">Indicates that the output type has been set on the capture engine in response to [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="data-type"></a><span data-ttu-id="09180-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="09180-105">Data type</span></span>

<span data-ttu-id="09180-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="09180-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="09180-107">備註</span><span class="sxs-lookup"><span data-stu-id="09180-107">Remarks</span></span>

<span data-ttu-id="09180-108">您可以呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) ，找出作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="09180-108">You can call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) to find out if the operation was successful or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="09180-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="09180-109">Requirements</span></span>



| <span data-ttu-id="09180-110">需求</span><span class="sxs-lookup"><span data-stu-id="09180-110">Requirement</span></span> | <span data-ttu-id="09180-111">值</span><span class="sxs-lookup"><span data-stu-id="09180-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09180-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09180-112">Minimum supported client</span></span><br/> | <span data-ttu-id="09180-113">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09180-113">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="09180-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09180-114">Minimum supported server</span></span><br/> | <span data-ttu-id="09180-115">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09180-115">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09180-116">標頭</span><span class="sxs-lookup"><span data-stu-id="09180-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="09180-117"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="09180-117"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="09180-118">Idl</span><span class="sxs-lookup"><span data-stu-id="09180-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09180-119"><dt>Mfcaptureengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="09180-119"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09180-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09180-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09180-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="09180-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09180-122">**IMFCaptureSink2::SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="09180-122">**IMFCaptureSink2::SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




