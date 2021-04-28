---
description: NtGdiDdAddAttachedSurface 函式-將介面附加至另一個介面。
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: 'NtGdiDdAddAttachedSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085786"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="e4a20-103">NtGdiDdAddAttachedSurface 函式</span><span class="sxs-lookup"><span data-stu-id="e4a20-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="e4a20-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="e4a20-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e4a20-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e4a20-106">將介面附加至另一個介面。</span><span class="sxs-lookup"><span data-stu-id="e4a20-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a20-107">語法</span><span class="sxs-lookup"><span data-stu-id="e4a20-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="e4a20-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4a20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a20-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a20-110">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，代表另一個介面所連接的介面。</span><span class="sxs-lookup"><span data-stu-id="e4a20-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="e4a20-111">*hSurfaceAttached* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a20-112">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，代表要附加的介面。</span><span class="sxs-lookup"><span data-stu-id="e4a20-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="e4a20-113">*puAddAttachedSurfaceData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a20-114">[**DD \_ ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata)結構的指標，其中包含驅動程式執行附件所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="e4a20-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a20-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4a20-115">Return value</span></span>

<span data-ttu-id="e4a20-116">**NtGdiDdAddAttachedSurface** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="e4a20-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e4a20-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e4a20-117">Return code</span></span>                                                                                              | <span data-ttu-id="e4a20-118">Description</span><span class="sxs-lookup"><span data-stu-id="e4a20-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4a20-119"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a20-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e4a20-120">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="e4a20-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e4a20-121">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="e4a20-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e4a20-122">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="e4a20-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e4a20-123"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a20-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e4a20-124">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="e4a20-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e4a20-125">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="e4a20-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e4a20-126">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="e4a20-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4a20-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4a20-127">Requirements</span></span>



| <span data-ttu-id="e4a20-128">需求</span><span class="sxs-lookup"><span data-stu-id="e4a20-128">Requirement</span></span> | <span data-ttu-id="e4a20-129">值</span><span class="sxs-lookup"><span data-stu-id="e4a20-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a20-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4a20-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a20-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e4a20-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4a20-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a20-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4a20-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e4a20-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e4a20-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a20-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a20-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4a20-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4a20-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a20-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="e4a20-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
