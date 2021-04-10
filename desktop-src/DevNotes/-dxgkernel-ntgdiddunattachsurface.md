---
description: 移除在兩個核心模式介面物件之間，以 NtGdiDdAttachSurface 建立的附件。
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: 'NtGdiDdUnattachSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936094"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="09d99-103">NtGdiDdUnattachSurface 函式</span><span class="sxs-lookup"><span data-stu-id="09d99-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="09d99-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="09d99-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="09d99-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="09d99-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="09d99-106">移除在兩個核心模式介面物件之間，以 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)建立的附件。</span><span class="sxs-lookup"><span data-stu-id="09d99-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d99-107">語法</span><span class="sxs-lookup"><span data-stu-id="09d99-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="09d99-108">參數</span><span class="sxs-lookup"><span data-stu-id="09d99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d99-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09d99-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d99-110">以 hSurfaceFrom 參數形式傳遞至 [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)的核心模式介面物件。</span><span class="sxs-lookup"><span data-stu-id="09d99-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="09d99-111">*hSurfaceAttached* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09d99-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d99-112">以 hSurfaceTo 參數形式傳遞至 NtGdiDdAttachSurface 的核心模式介面物件[ ](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="09d99-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d99-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="09d99-113">Return value</span></span>

<span data-ttu-id="09d99-114">**NtGdiDdUnattachSurface** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="09d99-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="09d99-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="09d99-115">Return code</span></span>                                                                                              | <span data-ttu-id="09d99-116">Description</span><span class="sxs-lookup"><span data-stu-id="09d99-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09d99-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="09d99-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="09d99-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="09d99-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="09d99-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="09d99-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="09d99-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="09d99-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="09d99-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="09d99-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="09d99-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="09d99-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="09d99-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="09d99-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="09d99-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="09d99-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09d99-125">備註</span><span class="sxs-lookup"><span data-stu-id="09d99-125">Remarks</span></span>

<span data-ttu-id="09d99-126">建議應用程式使用 DirectDraw API，以較高層級的方式處理介面附件。</span><span class="sxs-lookup"><span data-stu-id="09d99-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="09d99-127">不需要呼叫此函式，因為在呼叫 [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) 時，核心會自動終結所有的附件。</span><span class="sxs-lookup"><span data-stu-id="09d99-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d99-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="09d99-128">Requirements</span></span>



| <span data-ttu-id="09d99-129">需求</span><span class="sxs-lookup"><span data-stu-id="09d99-129">Requirement</span></span> | <span data-ttu-id="09d99-130">值</span><span class="sxs-lookup"><span data-stu-id="09d99-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09d99-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09d99-131">Minimum supported client</span></span><br/> | <span data-ttu-id="09d99-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d99-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="09d99-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09d99-133">Minimum supported server</span></span><br/> | <span data-ttu-id="09d99-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d99-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09d99-135">標頭</span><span class="sxs-lookup"><span data-stu-id="09d99-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d99-136"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="09d99-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d99-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09d99-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d99-138">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="09d99-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




