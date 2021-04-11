---
description: 轉譯基本專案，並傳回更新後的呈現狀態。
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: 'NtGdiD3DDrawPrimitives2 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025859"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="5d364-103">NtGdiD3DDrawPrimitives2 函式</span><span class="sxs-lookup"><span data-stu-id="5d364-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="5d364-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="5d364-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5d364-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="5d364-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5d364-106">轉譯基本專案，並傳回更新後的呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="5d364-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d364-107">語法</span><span class="sxs-lookup"><span data-stu-id="5d364-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="5d364-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d364-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d364-109">*hCmdBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d364-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-110">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，識別包含命令資料的 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="5d364-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-111">*hVBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d364-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-112">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，識別包含頂點資料的 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="5d364-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-113">*pded* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5d364-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-114">[**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/)結構的指標，其中包含驅動程式呈現一或多個基本專案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="5d364-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-115">*pfpVidMemCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5d364-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-116">如果驅動程式交換命令緩衝區，則為視訊記憶體的新指標。</span><span class="sxs-lookup"><span data-stu-id="5d364-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-117">*pdwSizeCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5d364-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-118">指定驅動程式必須增加交換命令緩衝區的最小位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5d364-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-119">*pfpVidMemVtx* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5d364-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-120">如果驅動程式交換了頂點緩衝區，則為視訊記憶體的新指標。</span><span class="sxs-lookup"><span data-stu-id="5d364-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5d364-121">*pdwSizeVtx* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5d364-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d364-122">指定驅動程式必須為交換頂點緩衝區配置的最小位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5d364-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d364-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d364-123">Return value</span></span>

<span data-ttu-id="5d364-124">**NtGdiD3DDrawPrimitives2** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="5d364-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="5d364-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5d364-125">Return code</span></span>                                                                                              | <span data-ttu-id="5d364-126">Description</span><span class="sxs-lookup"><span data-stu-id="5d364-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d364-127"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="5d364-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="5d364-128">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="5d364-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="5d364-129">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="5d364-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="5d364-130">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="5d364-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="5d364-131"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="5d364-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="5d364-132">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="5d364-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="5d364-133">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="5d364-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="5d364-134">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="5d364-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d364-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d364-135">Requirements</span></span>



| <span data-ttu-id="5d364-136">需求</span><span class="sxs-lookup"><span data-stu-id="5d364-136">Requirement</span></span> | <span data-ttu-id="5d364-137">值</span><span class="sxs-lookup"><span data-stu-id="5d364-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d364-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d364-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5d364-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d364-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5d364-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d364-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5d364-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d364-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d364-142">標頭</span><span class="sxs-lookup"><span data-stu-id="5d364-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d364-143"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d364-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d364-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d364-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d364-145">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="5d364-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
