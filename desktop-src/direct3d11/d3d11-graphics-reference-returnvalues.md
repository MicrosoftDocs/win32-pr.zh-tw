---
title: Direct3D 11 傳回碼
description: API 函數的傳回碼。
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4130ed07faaabfd24bb48454d4e450f307c7a12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023613"
---
# <a name="direct3d-11-return-codes"></a><span data-ttu-id="9a07d-103">Direct3D 11 傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a07d-103">Direct3D 11 Return Codes</span></span>

<span data-ttu-id="9a07d-104">從 API 函式傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9a07d-104">Return codes from API functions.</span></span>

| <span data-ttu-id="9a07d-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9a07d-105">HRESULT</span></span> | <span data-ttu-id="9a07d-106">Description</span><span class="sxs-lookup"><span data-stu-id="9a07d-106">Description</span></span> |
|-|-|
| <span data-ttu-id="9a07d-107">D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) </span><span class="sxs-lookup"><span data-stu-id="9a07d-107">D3D11_ERROR_FILE_NOT_FOUND (0x887C0002)</span></span> | <span data-ttu-id="9a07d-108">找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="9a07d-108">The file was not found.</span></span> |
| <span data-ttu-id="9a07d-109">D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) </span><span class="sxs-lookup"><span data-stu-id="9a07d-109">D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001)</span></span> | <span data-ttu-id="9a07d-110">特定類型之狀態物件的唯一實例太多。</span><span class="sxs-lookup"><span data-stu-id="9a07d-110">There are too many unique instances of a particular type of state object.</span></span> |
| <span data-ttu-id="9a07d-111">D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) </span><span class="sxs-lookup"><span data-stu-id="9a07d-111">D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003)</span></span> | <span data-ttu-id="9a07d-112">特定類型之 view 物件的唯一實例太多。</span><span class="sxs-lookup"><span data-stu-id="9a07d-112">There are too many unique instances of a particular type of view object.</span></span> |
| <span data-ttu-id="9a07d-113">D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) </span><span class="sxs-lookup"><span data-stu-id="9a07d-113">D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004)</span></span> | <span data-ttu-id="9a07d-114">不 D3D11_MAP_WRITE_DISCARD 每個資源的 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)或 [**>id3d11devicecoNtext：： FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist)之後第一次呼叫 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 。</span><span class="sxs-lookup"><span data-stu-id="9a07d-114">The first call to [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) after either [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) or [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) per Resource was not D3D11_MAP_WRITE_DISCARD.</span></span> |
| <span data-ttu-id="9a07d-115">D3DERR_INVALIDCALL (取代為 DXGI_ERROR_INVALID_CALL)  (0x887A0001) </span><span class="sxs-lookup"><span data-stu-id="9a07d-115">D3DERR_INVALIDCALL (replaced with DXGI_ERROR_INVALID_CALL) (0x887A0001)</span></span> | <span data-ttu-id="9a07d-116">方法呼叫無效。</span><span class="sxs-lookup"><span data-stu-id="9a07d-116">The method call is invalid.</span></span> <span data-ttu-id="9a07d-117">例如，方法的參數可能不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="9a07d-117">For example, a method's parameter may not be a valid pointer.</span></span> |
| <span data-ttu-id="9a07d-118">D3DERR_WASSTILLDRAWING (取代為 DXGI_ERROR_WAS_STILL_DRAWING)  (0x887A000A) </span><span class="sxs-lookup"><span data-stu-id="9a07d-118">D3DERR_WASSTILLDRAWING (replaced with DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A)</span></span> | <span data-ttu-id="9a07d-119">先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。</span><span class="sxs-lookup"><span data-stu-id="9a07d-119">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span> |
| <span data-ttu-id="9a07d-120">E_FAIL (0x80004005)</span><span class="sxs-lookup"><span data-stu-id="9a07d-120">E_FAIL (0x80004005)</span></span> | <span data-ttu-id="9a07d-121">嘗試建立啟用了 debug 層的裝置，且未安裝該層。</span><span class="sxs-lookup"><span data-stu-id="9a07d-121">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="9a07d-122">E_INVALIDARG (0x80070057) </span><span class="sxs-lookup"><span data-stu-id="9a07d-122">E_INVALIDARG (0x80070057)</span></span> | <span data-ttu-id="9a07d-123">傳遞了不正確參數給傳回的函式。</span><span class="sxs-lookup"><span data-stu-id="9a07d-123">An invalid parameter was passed to the returning function.</span></span> |
| <span data-ttu-id="9a07d-124">E_OUTOFMEMORY (0x8007000E) </span><span class="sxs-lookup"><span data-stu-id="9a07d-124">E_OUTOFMEMORY (0x8007000E)</span></span> | <span data-ttu-id="9a07d-125">Direct3D 無法配置足夠的記憶體來完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="9a07d-125">Direct3D could not allocate sufficient memory to complete the call.</span></span> |
| <span data-ttu-id="9a07d-126">E_NOTIMPL (0x80004001) </span><span class="sxs-lookup"><span data-stu-id="9a07d-126">E_NOTIMPL (0x80004001)</span></span> | <span data-ttu-id="9a07d-127">未以傳遞的參數組合來執行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="9a07d-127">The method call isn't implemented with the passed parameter combination.</span></span> |
| <span data-ttu-id="9a07d-128">S_FALSE ( (HRESULT) 1L) </span><span class="sxs-lookup"><span data-stu-id="9a07d-128">S_FALSE ((HRESULT)1L)</span></span> | <span data-ttu-id="9a07d-129">替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。</span><span class="sxs-lookup"><span data-stu-id="9a07d-129">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="9a07d-130">S_OK ( (HRESULT) 0L) </span><span class="sxs-lookup"><span data-stu-id="9a07d-130">S_OK ((HRESULT)0L)</span></span> | <span data-ttu-id="9a07d-131">未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a07d-131">No error occurred.</span></span> |

<span data-ttu-id="9a07d-132">如需傳回碼的詳細資訊，請參閱 [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error)。</span><span class="sxs-lookup"><span data-stu-id="9a07d-132">For more return codes, see [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a07d-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a07d-133">Related topics</span></span>

* [<span data-ttu-id="9a07d-134">Direct3D 11 參考</span><span class="sxs-lookup"><span data-stu-id="9a07d-134">Direct3D 11 Reference</span></span>](d3d11-graphics-reference.md)