---
description: 可由 DXGI 函數傳回的狀態碼。
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: 'DXGI_STATUS (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993876"
---
# <a name="dxgi_status"></a><span data-ttu-id="5ee0f-103">DXGI \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="5ee0f-103">DXGI\_STATUS</span></span>

<span data-ttu-id="5ee0f-104">可由 DXGI 函數傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="5ee0f-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="5ee0f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="5ee0f-106">Description</span><span class="sxs-lookup"><span data-stu-id="5ee0f-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="5ee0f-107"><dt>**DXGI \_狀態 \_ pixels occluded**</dt> <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="5ee0f-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="5ee0f-108">視窗內容是不可見的。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-108">The window content is not visible.</span></span> <span data-ttu-id="5ee0f-109">收到此狀態時，應用程式可能會停止轉譯，並使用 DXGI \_ 目前的 \_ 測試來判斷何時要繼續轉譯。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="5ee0f-110">\_ \_ 如果您要使用翻轉模型交換鏈，您將不會收到 DXGI 狀態 pixels occluded。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="5ee0f-111"><dt>**DXGI \_狀態 \_ 模式 \_ 已變更**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="5ee0f-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="5ee0f-112">桌面顯示模式已變更，可能有色彩轉換/延展。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="5ee0f-113">應用程式應該呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) ，以符合新的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="5ee0f-114"><dt>**DXGI \_狀態 \_ 模式 \_ 變更 \_ \_ 進行中**</dt> <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="5ee0f-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="5ee0f-115">如果呼叫任一個 API 時， [**IDXGISwapChain：： ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)和 [**IDXGISwapChain：： SETFULLSCREENSTATE**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)會傳回 DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中。</span><span class="sxs-lookup"><span data-stu-id="5ee0f-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5ee0f-116">備註</span><span class="sxs-lookup"><span data-stu-id="5ee0f-116">Remarks</span></span>

<span data-ttu-id="5ee0f-117">每個 **DXGI \_ 狀態值** 的 **HRESULT** 值都是由 DXGItype 中定義的這個宏所決定：</span><span class="sxs-lookup"><span data-stu-id="5ee0f-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="5ee0f-118">例如，已將 **DXGI \_ 狀態 \_ Pixels occluded** 定義為 **0x087A0001**：</span><span class="sxs-lookup"><span data-stu-id="5ee0f-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="5ee0f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ee0f-119">Requirements</span></span>



| <span data-ttu-id="5ee0f-120">需求</span><span class="sxs-lookup"><span data-stu-id="5ee0f-120">Requirement</span></span> | <span data-ttu-id="5ee0f-121">值</span><span class="sxs-lookup"><span data-stu-id="5ee0f-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5ee0f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5ee0f-122">Header</span></span><br/> | <dl> <span data-ttu-id="5ee0f-123"><dt>DXGI。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee0f-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee0f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ee0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee0f-125">DXGI 常數</span><span class="sxs-lookup"><span data-stu-id="5ee0f-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




