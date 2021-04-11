---
description: 重新置放或修改重迭表面的視覺屬性。
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: 'NtGdiDdUpdateOverlay 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936093"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="d3f77-103">NtGdiDdUpdateOverlay 函式</span><span class="sxs-lookup"><span data-stu-id="d3f77-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="d3f77-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="d3f77-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d3f77-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d3f77-106">重新置放或修改重迭表面的視覺屬性。</span><span class="sxs-lookup"><span data-stu-id="d3f77-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f77-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3f77-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="d3f77-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3f77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f77-109">*hSurfaceDestination* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f77-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3f77-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="d3f77-111">*hSurfaceSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f77-112">描述重迭表面之 [**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3f77-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="d3f77-113">*puUpdateOverlayData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3f77-114">[**DD \_ UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata)結構的指標，其中包含更新覆迭所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="d3f77-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f77-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3f77-115">Return value</span></span>

<span data-ttu-id="d3f77-116">**NtGdiDdUpdateOverlay** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="d3f77-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d3f77-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d3f77-117">Return code</span></span>                                                                                              | <span data-ttu-id="d3f77-118">Description</span><span class="sxs-lookup"><span data-stu-id="d3f77-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3f77-119"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f77-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d3f77-120">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d3f77-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d3f77-121">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="d3f77-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d3f77-122">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="d3f77-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d3f77-123"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f77-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d3f77-124">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="d3f77-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d3f77-125">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="d3f77-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d3f77-126">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="d3f77-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3f77-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3f77-127">Requirements</span></span>



| <span data-ttu-id="d3f77-128">需求</span><span class="sxs-lookup"><span data-stu-id="d3f77-128">Requirement</span></span> | <span data-ttu-id="d3f77-129">值</span><span class="sxs-lookup"><span data-stu-id="d3f77-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f77-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3f77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f77-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d3f77-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3f77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f77-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3f77-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3f77-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d3f77-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f77-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f77-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f77-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3f77-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f77-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="d3f77-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
