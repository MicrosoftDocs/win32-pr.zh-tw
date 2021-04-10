---
description: 從 Microsoft DirectDraw 介面建立 Microsoft Direct3D 介面，並將要求的控制碼值與它產生關聯。
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: 'NtGdiDdCreateSurfaceEx 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110128"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="b69a8-103">NtGdiDdCreateSurfaceEx 函式</span><span class="sxs-lookup"><span data-stu-id="b69a8-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="b69a8-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="b69a8-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b69a8-105">相反地，請使用 DirectDraw 和 Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b69a8-106">從 Microsoft DirectDraw 介面建立 Microsoft Direct3D 介面，並將要求的控制碼值與它產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b69a8-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="b69a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="b69a8-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="b69a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="b69a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b69a8-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b69a8-110">應用程式所建立之 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b69a8-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="b69a8-111">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b69a8-112">針對 Direct3D 建立的 DirectDraw 介面控制碼。</span><span class="sxs-lookup"><span data-stu-id="b69a8-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="b69a8-113">這些控制碼在每個不同的 [**DD \_ DIRECTDRAW \_ 本機**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) 結構內都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b69a8-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b69a8-114">*dwSurfaceHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b69a8-115">[**DD \_ CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata)結構的控制碼，其中包含驅動程式建立介面所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="b69a8-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b69a8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b69a8-116">Return value</span></span>

<span data-ttu-id="b69a8-117">**NtGdiDdCreateSurfaceEx** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="b69a8-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b69a8-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b69a8-118">Return code</span></span>                                                                                              | <span data-ttu-id="b69a8-119">Description</span><span class="sxs-lookup"><span data-stu-id="b69a8-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b69a8-120"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="b69a8-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b69a8-121">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="b69a8-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b69a8-122">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="b69a8-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b69a8-123">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="b69a8-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b69a8-124"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="b69a8-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b69a8-125">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="b69a8-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b69a8-126">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="b69a8-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b69a8-127">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="b69a8-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b69a8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b69a8-128">Requirements</span></span>



| <span data-ttu-id="b69a8-129">需求</span><span class="sxs-lookup"><span data-stu-id="b69a8-129">Requirement</span></span> | <span data-ttu-id="b69a8-130">值</span><span class="sxs-lookup"><span data-stu-id="b69a8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b69a8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b69a8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b69a8-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b69a8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b69a8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b69a8-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b69a8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b69a8-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b69a8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b69a8-136"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b69a8-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b69a8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b69a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b69a8-138">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="b69a8-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
