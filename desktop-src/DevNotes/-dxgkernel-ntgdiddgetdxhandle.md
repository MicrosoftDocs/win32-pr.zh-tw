---
description: 傳回核心模式 Microsoft DirectX API 控制碼，以用於對控制 DirectX API 機制之核心模式進入點的後續呼叫中使用。
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: 'NtGdiDdGetDxHandle 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973384"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="34748-103">NtGdiDdGetDxHandle 函式</span><span class="sxs-lookup"><span data-stu-id="34748-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="34748-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="34748-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="34748-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="34748-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="34748-106">傳回核心模式 Microsoft DirectX API 控制碼，以用於對控制 DirectX API 機制之核心模式進入點的後續呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="34748-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="34748-107">語法</span><span class="sxs-lookup"><span data-stu-id="34748-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="34748-108">參數</span><span class="sxs-lookup"><span data-stu-id="34748-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34748-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34748-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34748-110">擁有介面之 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="34748-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="34748-111">這個參數是選擇性的，可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="34748-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34748-112">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34748-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34748-113">要傳回核心模式 DirectX API 控制碼的介面。</span><span class="sxs-lookup"><span data-stu-id="34748-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="34748-114">這個參數是選擇性的，可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="34748-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34748-115">*bRelease* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34748-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34748-116">如果應該釋放 DirectX API 核心模式介面，則設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="34748-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="34748-117">否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="34748-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34748-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="34748-118">Return value</span></span>

<span data-ttu-id="34748-119">用於後續 DirectX API 導向核心進入點的 DirectX API 控制碼。</span><span class="sxs-lookup"><span data-stu-id="34748-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="34748-120">備註</span><span class="sxs-lookup"><span data-stu-id="34748-120">Remarks</span></span>

<span data-ttu-id="34748-121">如果同時指定 *hDirectDraw* 和 *hSurface* ，則會忽略 *hSurface* 。</span><span class="sxs-lookup"><span data-stu-id="34748-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="34748-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="34748-122">Requirements</span></span>



| <span data-ttu-id="34748-123">需求</span><span class="sxs-lookup"><span data-stu-id="34748-123">Requirement</span></span> | <span data-ttu-id="34748-124">值</span><span class="sxs-lookup"><span data-stu-id="34748-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34748-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34748-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34748-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34748-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="34748-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34748-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34748-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34748-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34748-129">標頭</span><span class="sxs-lookup"><span data-stu-id="34748-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34748-130"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="34748-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34748-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34748-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34748-132">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="34748-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




