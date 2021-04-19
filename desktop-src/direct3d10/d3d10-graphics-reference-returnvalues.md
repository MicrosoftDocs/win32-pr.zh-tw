---
description: 下表包含 API 函數的傳回碼。
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Direct3D 10 傳回碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972769"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="42999-103">Direct3D 10 傳回碼</span><span class="sxs-lookup"><span data-stu-id="42999-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="42999-104">下表包含 API 函數的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="42999-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="42999-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="42999-105">HRESULT</span></span>                                         | <span data-ttu-id="42999-106">Description</span><span class="sxs-lookup"><span data-stu-id="42999-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42999-107">\_ \_ \_ \_ 找不到 D3D10 錯誤檔案</span><span class="sxs-lookup"><span data-stu-id="42999-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="42999-108">找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="42999-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="42999-109">D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="42999-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="42999-110">特定類型之 [狀態物件](d3d10-graphics-programming-guide-api-features-state-objects.md)的唯一實例太多。</span><span class="sxs-lookup"><span data-stu-id="42999-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="42999-111">D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="42999-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="42999-112">方法呼叫無效。</span><span class="sxs-lookup"><span data-stu-id="42999-112">The method call is invalid.</span></span> <span data-ttu-id="42999-113">例如，方法的參數可能不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="42999-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="42999-114">D3DERR \_ WASSTILLDRAWING</span><span class="sxs-lookup"><span data-stu-id="42999-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="42999-115">先前正在將資訊傳送到或從此表面傳送的 array.blit 作業不完整。</span><span class="sxs-lookup"><span data-stu-id="42999-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="42999-116">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="42999-116">E\_FAIL</span></span>                                         | <span data-ttu-id="42999-117">嘗試建立啟用了 [debug 層](d3d10-graphics-programming-guide-api-features-layers.md) 的裝置，且未安裝該層。</span><span class="sxs-lookup"><span data-stu-id="42999-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="42999-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="42999-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="42999-119">傳遞了不正確參數給傳回的函式。</span><span class="sxs-lookup"><span data-stu-id="42999-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="42999-120">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="42999-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="42999-121">Direct3D 無法配置足夠的記憶體來完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="42999-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="42999-122">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="42999-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="42999-123">未以傳遞的參數組合來執行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="42999-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="42999-124">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="42999-124">S\_FALSE</span></span>                                        | <span data-ttu-id="42999-125">替代成功值，表示成功但非標準完成 (精確的意義取決於內容) 。</span><span class="sxs-lookup"><span data-stu-id="42999-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="42999-126">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="42999-126">S\_OK</span></span>                                           | <span data-ttu-id="42999-127">未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="42999-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="42999-128">若要撰寫可妥善處理 [HRESULT 值](../winprog/windows-data-types.md) 的程式碼，請使用成功的 (hr) 和失敗 (hr) 宏。</span><span class="sxs-lookup"><span data-stu-id="42999-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42999-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="42999-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42999-130">Direct3D 參考</span><span class="sxs-lookup"><span data-stu-id="42999-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="42999-131">Direct3D 10 的參考</span><span class="sxs-lookup"><span data-stu-id="42999-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
