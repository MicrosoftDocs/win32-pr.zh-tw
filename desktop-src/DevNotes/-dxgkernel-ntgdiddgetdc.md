---
description: 為指定的介面建立 (DC) 的裝置內容。
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: 'NtGdiDdGetDC 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110669"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="925b1-103">NtGdiDdGetDC 函式</span><span class="sxs-lookup"><span data-stu-id="925b1-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="925b1-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="925b1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="925b1-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="925b1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="925b1-106">為指定的介面建立 (DC) 的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="925b1-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="925b1-107">語法</span><span class="sxs-lookup"><span data-stu-id="925b1-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="925b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="925b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925b1-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="925b1-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="925b1-110">[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)或 [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)先前傳回之核心模式 DirectDraw 介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="925b1-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="925b1-111">*puColorTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="925b1-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="925b1-112">傳回之 DC 的覆寫色彩表指標。</span><span class="sxs-lookup"><span data-stu-id="925b1-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925b1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="925b1-113">Return value</span></span>

<span data-ttu-id="925b1-114">如果成功，此函式會傳回有效的 **HDC**;否則，它會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="925b1-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="925b1-115">備註</span><span class="sxs-lookup"><span data-stu-id="925b1-115">Remarks</span></span>

<span data-ttu-id="925b1-116">在任何指定時間，每個介面只允許一個 DC。</span><span class="sxs-lookup"><span data-stu-id="925b1-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="925b1-117">**NtGdiDdGetDC** 的後續呼叫將會失敗，直到釋放先前的 DC 為止。</span><span class="sxs-lookup"><span data-stu-id="925b1-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="925b1-118">建議應用程式改為呼叫 [IDirectDrawSurface7：： GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) ，以與作業系統無關的方式提供相同的功能。</span><span class="sxs-lookup"><span data-stu-id="925b1-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="925b1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="925b1-119">Requirements</span></span>



| <span data-ttu-id="925b1-120">需求</span><span class="sxs-lookup"><span data-stu-id="925b1-120">Requirement</span></span> | <span data-ttu-id="925b1-121">值</span><span class="sxs-lookup"><span data-stu-id="925b1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="925b1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="925b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="925b1-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="925b1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="925b1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="925b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="925b1-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="925b1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="925b1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="925b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="925b1-127"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="925b1-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="925b1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="925b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925b1-129">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="925b1-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="925b1-130">**DdGetDC**</span><span class="sxs-lookup"><span data-stu-id="925b1-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
