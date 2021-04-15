---
description: 鎖定介面記憶體的指定區域，並提供與介面相關聯之記憶體區塊的有效指標。
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: 'NtGdiDdLock 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3ddf40ae992b6b463886396ba026ec08293bb027
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468040"
---
# <a name="ntgdiddlock-function"></a><span data-ttu-id="d431e-103">NtGdiDdLock 函式</span><span class="sxs-lookup"><span data-stu-id="d431e-103">NtGdiDdLock function</span></span>

<span data-ttu-id="d431e-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="d431e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d431e-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="d431e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d431e-106">鎖定介面記憶體的指定區域，並提供與介面相關聯之記憶體區塊的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d431e-106">Locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d431e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d431e-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a><span data-ttu-id="d431e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d431e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d431e-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d431e-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d431e-110">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，描述與要鎖定之記憶體區域相關聯的介面。</span><span class="sxs-lookup"><span data-stu-id="d431e-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="d431e-111">*puLockData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d431e-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d431e-112">[**DD \_ LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata)結構的指標，其中包含執行鎖定所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="d431e-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lockdown.</span></span>

</dd> <dt>

<span data-ttu-id="d431e-113">*hdcClip* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d431e-113">*hdcClip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d431e-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="d431e-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d431e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d431e-115">Return value</span></span>

<span data-ttu-id="d431e-116">**NtGdiDdLock** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="d431e-116">**NtGdiDdLock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d431e-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d431e-117">Return code</span></span>                                                                                              | <span data-ttu-id="d431e-118">Description</span><span class="sxs-lookup"><span data-stu-id="d431e-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d431e-119"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="d431e-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d431e-120">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d431e-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d431e-121">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="d431e-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d431e-122">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="d431e-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d431e-123"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="d431e-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d431e-124">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="d431e-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d431e-125">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="d431e-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d431e-126">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="d431e-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d431e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d431e-127">Requirements</span></span>



| <span data-ttu-id="d431e-128">需求</span><span class="sxs-lookup"><span data-stu-id="d431e-128">Requirement</span></span> | <span data-ttu-id="d431e-129">值</span><span class="sxs-lookup"><span data-stu-id="d431e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d431e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d431e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d431e-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d431e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d431e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d431e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d431e-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d431e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d431e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d431e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d431e-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d431e-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d431e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d431e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d431e-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="d431e-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
