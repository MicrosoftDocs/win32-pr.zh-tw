---
description: 終結先前配置的核心模式 Microsoft DirectDraw 介面物件。
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: 'NtGdiDdDestroySurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025915"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="aa6d3-103">NtGdiDdDestroySurface 函式</span><span class="sxs-lookup"><span data-stu-id="aa6d3-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="aa6d3-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="aa6d3-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="aa6d3-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="aa6d3-106">終結先前配置的核心模式 Microsoft DirectDraw 介面物件。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6d3-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa6d3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="aa6d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa6d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6d3-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa6d3-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6d3-110">先前配置之核心模式介面物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="aa6d3-111">*bRealDestroy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa6d3-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6d3-112">指定如何終結表面。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="aa6d3-113">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="aa6d3-114"> (TRUE) </span><span class="sxs-lookup"><span data-stu-id="aa6d3-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="aa6d3-115">終結表面和可用的視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="aa6d3-116"> (FALSE) </span><span class="sxs-lookup"><span data-stu-id="aa6d3-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="aa6d3-117">釋放視訊記憶體，但讓表面保持未初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6d3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa6d3-118">Return value</span></span>

<span data-ttu-id="aa6d3-119">**NtGdiDdDestroySurface** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="aa6d3-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aa6d3-120">Return code</span></span>                                                                                              | <span data-ttu-id="aa6d3-121">Description</span><span class="sxs-lookup"><span data-stu-id="aa6d3-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa6d3-122"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="aa6d3-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="aa6d3-123">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="aa6d3-124">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="aa6d3-125">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="aa6d3-126"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="aa6d3-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="aa6d3-127">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="aa6d3-128">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="aa6d3-129">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa6d3-130">備註</span><span class="sxs-lookup"><span data-stu-id="aa6d3-130">Remarks</span></span>

<span data-ttu-id="aa6d3-131">建議應用程式使用 DirectDraw 和 Direct3D Api 來建立和終結介面，而不是此函數。</span><span class="sxs-lookup"><span data-stu-id="aa6d3-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6d3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa6d3-132">Requirements</span></span>



| <span data-ttu-id="aa6d3-133">需求</span><span class="sxs-lookup"><span data-stu-id="aa6d3-133">Requirement</span></span> | <span data-ttu-id="aa6d3-134">值</span><span class="sxs-lookup"><span data-stu-id="aa6d3-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6d3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa6d3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6d3-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa6d3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="aa6d3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa6d3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6d3-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa6d3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aa6d3-139">標頭</span><span class="sxs-lookup"><span data-stu-id="aa6d3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa6d3-140"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa6d3-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa6d3-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa6d3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6d3-142">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="aa6d3-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




