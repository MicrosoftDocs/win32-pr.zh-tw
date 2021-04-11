---
description: 判斷是否發生了最近在表面上要求的翻轉。
ms.assetid: 4489e259-b22d-4e72-807a-5290401f0331
title: 'NtGdiDdGetFlipStatus 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetFlipStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 49ef59fd110c315b3111252084a3c60ddf4cd598
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847276"
---
# <a name="ntgdiddgetflipstatus-function"></a><span data-ttu-id="18800-103">NtGdiDdGetFlipStatus 函式</span><span class="sxs-lookup"><span data-stu-id="18800-103">NtGdiDdGetFlipStatus function</span></span>

<span data-ttu-id="18800-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="18800-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="18800-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="18800-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="18800-106">判斷是否發生了最近在表面上要求的翻轉。</span><span class="sxs-lookup"><span data-stu-id="18800-106">Determines whether the most recently requested flip on a surface has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="18800-107">語法</span><span class="sxs-lookup"><span data-stu-id="18800-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetFlipStatus(
  _In_    HANDLE                hSurface,
  _Inout_ PDD_GETFLIPSTATUSDATA puGetFlipStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="18800-108">參數</span><span class="sxs-lookup"><span data-stu-id="18800-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18800-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18800-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18800-110">[DD \_ 介面 \_ 區域](https://msdn.microsoft.com/library/ms793861.aspx)結構的控制碼，描述正在查詢其翻轉狀態的介面。</span><span class="sxs-lookup"><span data-stu-id="18800-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure that describes the surface whose flip status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="18800-111">*puGetFlipStatusData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="18800-111">*puGetFlipStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18800-112">[DD \_ GETFLIPSTATUSDATA](https://msdn.microsoft.com/library/ms793859.aspx)結構的指標，其中包含執行 flip status 查詢所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="18800-112">Pointer to a [DD\_GETFLIPSTATUSDATA](https://msdn.microsoft.com/library/ms793859.aspx) structure that contains the information required to perform the flip status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18800-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="18800-113">Return value</span></span>

<span data-ttu-id="18800-114">**NtGdiDdGetFlipStatus** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="18800-114">**NtGdiDdGetFlipStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="18800-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="18800-115">Return code</span></span>                                                                                              | <span data-ttu-id="18800-116">Description</span><span class="sxs-lookup"><span data-stu-id="18800-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18800-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="18800-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="18800-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="18800-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="18800-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="18800-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="18800-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="18800-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="18800-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="18800-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="18800-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="18800-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="18800-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="18800-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="18800-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="18800-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18800-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="18800-125">Requirements</span></span>



| <span data-ttu-id="18800-126">需求</span><span class="sxs-lookup"><span data-stu-id="18800-126">Requirement</span></span> | <span data-ttu-id="18800-127">值</span><span class="sxs-lookup"><span data-stu-id="18800-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18800-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18800-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18800-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18800-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="18800-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18800-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18800-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18800-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18800-132">標頭</span><span class="sxs-lookup"><span data-stu-id="18800-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="18800-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="18800-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18800-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18800-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18800-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="18800-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




