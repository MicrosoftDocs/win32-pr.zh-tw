---
title: Direct3D 12 傳回碼
description: 以下是來自 API 函數的傳回碼。
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968298"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="a5e69-103">Direct3D 12 傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5e69-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="a5e69-104">以下是來自 API 函數的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a5e69-104">The following are return codes from API functions.</span></span> <span data-ttu-id="a5e69-105">如需傳回碼的詳細資訊，請參閱 [DXGI \_ 錯誤](/windows/desktop/direct3ddxgi/dxgi-error)。</span><span class="sxs-lookup"><span data-stu-id="a5e69-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="a5e69-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a5e69-106">HRESULT</span></span>                                                                  | <span data-ttu-id="a5e69-107">Description</span><span class="sxs-lookup"><span data-stu-id="a5e69-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e69-108">\_ \_ \_ 找不到 D3D12 錯誤介面卡 \_</span><span class="sxs-lookup"><span data-stu-id="a5e69-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="a5e69-109">指定的快取 PSO 是在不同的介面卡上建立的，無法在目前的介面卡上重複使用。</span><span class="sxs-lookup"><span data-stu-id="a5e69-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="a5e69-110">D3D12 \_ 錯誤 \_ 驅動程式 \_ 版本 \_ 不符</span><span class="sxs-lookup"><span data-stu-id="a5e69-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="a5e69-111">指定的快取 PSO 是在不同的驅動程式版本上建立的，無法在目前的介面卡上重複使用。</span><span class="sxs-lookup"><span data-stu-id="a5e69-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="a5e69-112">D3DERR \_ INVALIDCALL (取代了 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫) </span><span class="sxs-lookup"><span data-stu-id="a5e69-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="a5e69-113">方法呼叫無效。</span><span class="sxs-lookup"><span data-stu-id="a5e69-113">The method call is invalid.</span></span> <span data-ttu-id="a5e69-114">例如，方法的參數可能不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="a5e69-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="a5e69-115">D3DERR \_ WASSTILLDRAWING (取代了 DXGI \_ 錯誤 \_ ， \_ 仍在 \_ 繪圖中) </span><span class="sxs-lookup"><span data-stu-id="a5e69-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="a5e69-116">先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。</span><span class="sxs-lookup"><span data-stu-id="a5e69-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="a5e69-117">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="a5e69-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="a5e69-118">嘗試建立啟用了 debug 層的裝置，且未安裝該層。</span><span class="sxs-lookup"><span data-stu-id="a5e69-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="a5e69-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a5e69-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="a5e69-120">傳遞了不正確參數給傳回的函式。</span><span class="sxs-lookup"><span data-stu-id="a5e69-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="a5e69-121">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="a5e69-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="a5e69-122">Direct3D 無法配置足夠的記憶體來完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="a5e69-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="a5e69-123">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a5e69-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="a5e69-124">未以傳遞的參數組合來執行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="a5e69-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="a5e69-125">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="a5e69-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="a5e69-126">替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。</span><span class="sxs-lookup"><span data-stu-id="a5e69-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="a5e69-127">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="a5e69-127">S\_OK</span></span>                                                                    | <span data-ttu-id="a5e69-128">未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5e69-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a5e69-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5e69-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e69-130">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="a5e69-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 