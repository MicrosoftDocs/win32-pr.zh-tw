---
description: 導致與目標和目前表面相關聯的介面記憶體被交換。
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: 'NtGdiDdFlip 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847280"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="6af31-103">NtGdiDdFlip 函式</span><span class="sxs-lookup"><span data-stu-id="6af31-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="6af31-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="6af31-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6af31-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="6af31-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6af31-106">導致與目標和目前表面相關聯的介面記憶體被交換。</span><span class="sxs-lookup"><span data-stu-id="6af31-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af31-107">語法</span><span class="sxs-lookup"><span data-stu-id="6af31-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="6af31-108">參數</span><span class="sxs-lookup"><span data-stu-id="6af31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af31-109">*hSurfaceCurrent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6af31-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af31-110">描述目前介面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6af31-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="6af31-111">*hSurfaceTarget* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6af31-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af31-112">描述目標介面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼，也就是驅動程式應該翻轉的介面。</span><span class="sxs-lookup"><span data-stu-id="6af31-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="6af31-113">*hSurfaceCurrentLeft* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6af31-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af31-114">描述目前左表面之 [DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6af31-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="6af31-115">*hSurfaceTargetLeft* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6af31-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af31-116">[DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx)結構的控制碼，描述要翻轉至的左側目標介面。</span><span class="sxs-lookup"><span data-stu-id="6af31-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="6af31-117">*puFlipData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6af31-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af31-118">[DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx)結構的指標，其中包含執行 flip 所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="6af31-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af31-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6af31-119">Return value</span></span>

<span data-ttu-id="6af31-120">**NtGdiDdFlip** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="6af31-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="6af31-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6af31-121">Return code</span></span>                                                                                              | <span data-ttu-id="6af31-122">Description</span><span class="sxs-lookup"><span data-stu-id="6af31-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6af31-123"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="6af31-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="6af31-124">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="6af31-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="6af31-125">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="6af31-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="6af31-126">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="6af31-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6af31-127"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="6af31-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="6af31-128">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="6af31-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="6af31-129">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="6af31-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="6af31-130">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="6af31-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6af31-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6af31-131">Requirements</span></span>



| <span data-ttu-id="6af31-132">需求</span><span class="sxs-lookup"><span data-stu-id="6af31-132">Requirement</span></span> | <span data-ttu-id="6af31-133">值</span><span class="sxs-lookup"><span data-stu-id="6af31-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6af31-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6af31-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6af31-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6af31-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6af31-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6af31-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6af31-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6af31-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6af31-138">標頭</span><span class="sxs-lookup"><span data-stu-id="6af31-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af31-139"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6af31-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6af31-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6af31-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af31-141">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="6af31-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




