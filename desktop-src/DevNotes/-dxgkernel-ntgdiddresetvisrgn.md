---
description: 用來啟用使用者模式，以對桌上型電腦上 windows 的裁剪區域有效瞭解。 這項裁剪可能會從使用者模式執行緒的觀點來非同步變更。
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: 'NtGdiDdResetVisrgn 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847028"
---
# <a name="ntgdiddresetvisrgn-function"></a><span data-ttu-id="5f96c-104">NtGdiDdResetVisrgn 函式</span><span class="sxs-lookup"><span data-stu-id="5f96c-104">NtGdiDdResetVisrgn function</span></span>

<span data-ttu-id="5f96c-105">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="5f96c-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5f96c-106">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="5f96c-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5f96c-107">用來啟用使用者模式，以對桌上型電腦上 windows 的裁剪區域有效瞭解。</span><span class="sxs-lookup"><span data-stu-id="5f96c-107">Used to enable the user mode to gain a valid understanding of the clipping region for windows on the desktop.</span></span> <span data-ttu-id="5f96c-108">這項裁剪可能會從使用者模式執行緒的觀點來非同步變更。</span><span class="sxs-lookup"><span data-stu-id="5f96c-108">This clipping can change asynchronously from the point of view of user-mode threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f96c-109">語法</span><span class="sxs-lookup"><span data-stu-id="5f96c-109">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="5f96c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f96c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f96c-111">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f96c-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f96c-112">屬於 DirectDraw 裝置之任何介面的使用者模式物件的指標，其為要重設剪切的物件。</span><span class="sxs-lookup"><span data-stu-id="5f96c-112">Pointer to the user-mode object of any surface belonging to the DirectDraw device for which clipping is to be reset.</span></span> <span data-ttu-id="5f96c-113">如需詳細資訊，請參閱 DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="5f96c-113">For details, see the DDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="5f96c-114">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f96c-114">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f96c-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="5f96c-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f96c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f96c-116">Return value</span></span>

<span data-ttu-id="5f96c-117">如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5f96c-117">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f96c-118">備註</span><span class="sxs-lookup"><span data-stu-id="5f96c-118">Remarks</span></span>

<span data-ttu-id="5f96c-119">從使用者模式執行緒的觀點來看，裁剪可能會以非同步方式變更。</span><span class="sxs-lookup"><span data-stu-id="5f96c-119">Clipping can change asynchronously from the point of view of user-mode threads.</span></span> <span data-ttu-id="5f96c-120">DirectDraw 和 Windows 圖形裝置介面的核心模式部分 (GDI) 維護計數器，此計數器會在整個桌面的剪切清單變更時遞增。</span><span class="sxs-lookup"><span data-stu-id="5f96c-120">The kernel-mode parts of DirectDraw and Windows Graphics Device Interface (GDI) maintain a counter that is incremented whenever the clipping list for the entire desktop changes.</span></span> <span data-ttu-id="5f96c-121">呼叫此函式會將此計數器記錄到系統上的每個現有 DirectDraw 主要介面。</span><span class="sxs-lookup"><span data-stu-id="5f96c-121">A call to this function records this counter with every existing DirectDraw primary surface on the system.</span></span>

<span data-ttu-id="5f96c-122">當 IDirectDrawSurface7：： Blt 或 IDirectDrawSurface7：： Lock 作業修改其中一個主要表面時， [：：](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) 或 [：： Lock](/previous-versions/ms858221(v=msdn.10)) 作業會進行修改， (查看 DDK 檔) ，則會將與此介面一起錄製的計數器與全域計數器進行比較。</span><span class="sxs-lookup"><span data-stu-id="5f96c-122">At any later time when one of these primary surfaces is modified by a [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) or [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) operation (see DDK documentation), then the counter recorded with the surface is compared with the global counter.</span></span> <span data-ttu-id="5f96c-123">如果這些值不同，則會將錯誤碼 DDERR \_ VISRGNCHANGED 傳回給使用者模式程式碼。</span><span class="sxs-lookup"><span data-stu-id="5f96c-123">If these values are different, an error code DDERR\_VISRGNCHANGED is returned to the user-mode code.</span></span> <span data-ttu-id="5f96c-124">然後，使用者模式程式碼將會重新查詢桌面目前的剪輯、呼叫 **NtGdiDdResetVisrgn**，然後重新嘗試套用至主要表面的 IDirectDrawSurface7：： Blt，並採用新的裁剪。</span><span class="sxs-lookup"><span data-stu-id="5f96c-124">The user-mode code will then re-query the current clipping for the desktop, call **NtGdiDdResetVisrgn**, and re-try the IDirectDrawSurface7::Blt applied to the primary surface, respecting the new clipping.</span></span> <span data-ttu-id="5f96c-125">最後，使用者模式程式碼所取樣的裁剪將會與核心模式所擁有的目前裁剪相同，而且會允許 IDirectDrawSurface7：： Blt 繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5f96c-125">Eventually, the clipping that was sampled by the user-mode code will be the same as the current clipping owned by kernel mode, and the IDirectDrawSurface7::Blt will be allowed to continue.</span></span>

<span data-ttu-id="5f96c-126">建議應用程式使用 [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) 介面或 [IDirect3DDevice8：:P](/previous-versions/ms889707(v=msdn.10)) 重新傳送的方法來處理非同步裁剪變更。</span><span class="sxs-lookup"><span data-stu-id="5f96c-126">Applications are advised to use the [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) interface or [IDirect3DDevice8::Present](/previous-versions/ms889707(v=msdn.10)) method to handle asynchronous clipping changes.</span></span> <span data-ttu-id="5f96c-127">這些結構會以自動化與作業系統無關的方式來執行非同步裁剪。</span><span class="sxs-lookup"><span data-stu-id="5f96c-127">These constructs implement asynchronous clipping in an automated and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f96c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f96c-128">Requirements</span></span>



| <span data-ttu-id="5f96c-129">需求</span><span class="sxs-lookup"><span data-stu-id="5f96c-129">Requirement</span></span> | <span data-ttu-id="5f96c-130">值</span><span class="sxs-lookup"><span data-stu-id="5f96c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f96c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f96c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5f96c-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f96c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5f96c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f96c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5f96c-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f96c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f96c-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5f96c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f96c-136"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f96c-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f96c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f96c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f96c-138">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="5f96c-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="5f96c-139">**DdResetVisrgn**</span><span class="sxs-lookup"><span data-stu-id="5f96c-139">**DdResetVisrgn**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
