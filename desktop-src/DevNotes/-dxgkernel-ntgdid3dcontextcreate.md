---
description: 建立內容。
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: 'NtGdiD3DCoNtextCreate 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110144"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="979b8-103">NtGdiD3DCoNtextCreate 函式</span><span class="sxs-lookup"><span data-stu-id="979b8-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="979b8-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="979b8-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="979b8-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="979b8-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="979b8-106">建立內容。</span><span class="sxs-lookup"><span data-stu-id="979b8-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="979b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="979b8-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="979b8-108">參數</span><span class="sxs-lookup"><span data-stu-id="979b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="979b8-109">*hDirectDrawLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="979b8-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="979b8-110">核心模式 DirectDraw 物件的控制碼，先前以 [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)建立，代表要建立 Direct3D 內容的裝置。</span><span class="sxs-lookup"><span data-stu-id="979b8-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="979b8-111">*hSurfColor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="979b8-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="979b8-112">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，描述要當做轉譯目標使用的 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="979b8-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="979b8-113">*hSurfZ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="979b8-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="979b8-114">[**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local)結構的控制碼，描述要當做深度緩衝區使用的 DirectDraw 介面。</span><span class="sxs-lookup"><span data-stu-id="979b8-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="979b8-115">如果這個成員是 **Null**，則不會執行深度緩衝。</span><span class="sxs-lookup"><span data-stu-id="979b8-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="979b8-116">*pdcci* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="979b8-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="979b8-117">[**D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/)結構的指標，其中包含建立內容所需的資訊，以及驅動程式應儲存在新內容中的資料。</span><span class="sxs-lookup"><span data-stu-id="979b8-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="979b8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="979b8-118">Return value</span></span>

<span data-ttu-id="979b8-119">**NtGdiD3DCoNtextCreate** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="979b8-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="979b8-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="979b8-120">Return code</span></span>                                                                                              | <span data-ttu-id="979b8-121">Description</span><span class="sxs-lookup"><span data-stu-id="979b8-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="979b8-122"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="979b8-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="979b8-123">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="979b8-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="979b8-124">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="979b8-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="979b8-125">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="979b8-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="979b8-126"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="979b8-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="979b8-127">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="979b8-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="979b8-128">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="979b8-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="979b8-129">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="979b8-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="979b8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="979b8-130">Requirements</span></span>



| <span data-ttu-id="979b8-131">需求</span><span class="sxs-lookup"><span data-stu-id="979b8-131">Requirement</span></span> | <span data-ttu-id="979b8-132">值</span><span class="sxs-lookup"><span data-stu-id="979b8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="979b8-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="979b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="979b8-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="979b8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="979b8-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="979b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="979b8-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="979b8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="979b8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="979b8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="979b8-138"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="979b8-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="979b8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="979b8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979b8-140">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="979b8-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
