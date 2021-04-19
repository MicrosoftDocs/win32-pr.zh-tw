---
description: 識別產生 capture 事件的元件。
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: 'MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984177"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="ff1dd-103">MF \_ 捕獲 \_ 引擎 \_ 事件產生器 \_ \_ GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="ff1dd-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="ff1dd-104">識別產生 capture 事件的元件。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="ff1dd-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ff1dd-105">Data type</span></span>

<span data-ttu-id="ff1dd-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ff1dd-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1dd-107">備註</span><span class="sxs-lookup"><span data-stu-id="ff1dd-107">Remarks</span></span>

<span data-ttu-id="ff1dd-108">這個屬性會出現在 capture 引擎的某些事件上。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="ff1dd-109">若要取得這個屬性，請在事件物件上呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) 。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="ff1dd-110">事件物件會透過 [**IMFCaptureEngineOnEventCallback：： OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) 方法傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="ff1dd-111">值是產生事件之元件的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="ff1dd-112">例如，值 **IID \_ IMFCapturePreviewSink** 表示預覽接收 ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)) 。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="ff1dd-113">並非每個 capture 事件都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ff1dd-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1dd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff1dd-114">Requirements</span></span>



| <span data-ttu-id="ff1dd-115">需求</span><span class="sxs-lookup"><span data-stu-id="ff1dd-115">Requirement</span></span> | <span data-ttu-id="ff1dd-116">值</span><span class="sxs-lookup"><span data-stu-id="ff1dd-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1dd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff1dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1dd-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff1dd-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ff1dd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff1dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1dd-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff1dd-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff1dd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ff1dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1dd-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1dd-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff1dd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff1dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1dd-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ff1dd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ff1dd-125">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="ff1dd-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="ff1dd-126">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="ff1dd-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




