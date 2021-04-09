---
description: 識別哪個資料流程產生了捕捉事件。
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: 'MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848530"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="49bfc-103">MF \_ CAPTURE \_ ENGINE \_ 事件 \_ 資料流程 \_ 索引屬性</span><span class="sxs-lookup"><span data-stu-id="49bfc-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="49bfc-104">識別哪個資料流程產生了捕捉事件。</span><span class="sxs-lookup"><span data-stu-id="49bfc-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="49bfc-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="49bfc-105">Data type</span></span>

<span data-ttu-id="49bfc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="49bfc-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="49bfc-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="49bfc-107">Get/set</span></span>

<span data-ttu-id="49bfc-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="49bfc-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="49bfc-109">備註</span><span class="sxs-lookup"><span data-stu-id="49bfc-109">Remarks</span></span>

<span data-ttu-id="49bfc-110">這個屬性會出現在 capture 引擎的某些事件上。</span><span class="sxs-lookup"><span data-stu-id="49bfc-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="49bfc-111">若要取得這個屬性，請在事件物件上呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 。</span><span class="sxs-lookup"><span data-stu-id="49bfc-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="49bfc-112">事件物件會透過 [**IMFCaptureEngineOnEventCallback：： OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) 方法傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="49bfc-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="49bfc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="49bfc-113">Requirements</span></span>



| <span data-ttu-id="49bfc-114">需求</span><span class="sxs-lookup"><span data-stu-id="49bfc-114">Requirement</span></span> | <span data-ttu-id="49bfc-115">值</span><span class="sxs-lookup"><span data-stu-id="49bfc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49bfc-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49bfc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49bfc-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49bfc-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="49bfc-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49bfc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49bfc-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49bfc-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="49bfc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="49bfc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49bfc-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="49bfc-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49bfc-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49bfc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49bfc-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="49bfc-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="49bfc-124">**IMFCaptureEngineOnEventCallback：： OnEvent**</span><span class="sxs-lookup"><span data-stu-id="49bfc-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




