---
description: 判斷驅動程式是否可以建立指定之描述的驅動程式層級命令或頂點緩衝區。
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: 'NtGdiDdCanCreateD3DBuffer 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991621"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="62f7d-103">NtGdiDdCanCreateD3DBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="62f7d-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="62f7d-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="62f7d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="62f7d-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="62f7d-106">判斷驅動程式是否可以建立指定之描述的驅動程式層級命令或頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="62f7d-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="62f7d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="62f7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="62f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f7d-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f7d-110">代表 DirectDraw 物件之 [**DD \_ DIRECTDRAW \_ 全域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62f7d-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="62f7d-111">*puCanCreateSurfaceData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62f7d-112">[**DD \_ CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="62f7d-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="62f7d-113">此結構包含驅動程式判斷是否可以建立命令或頂點緩衝區所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="62f7d-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f7d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="62f7d-114">Return value</span></span>

<span data-ttu-id="62f7d-115">**NtGdiDdCanCreateD3DBuffer** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="62f7d-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="62f7d-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="62f7d-116">Return code</span></span>                                                                                              | <span data-ttu-id="62f7d-117">Description</span><span class="sxs-lookup"><span data-stu-id="62f7d-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62f7d-118"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="62f7d-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="62f7d-119">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="62f7d-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="62f7d-120">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="62f7d-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="62f7d-121">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="62f7d-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="62f7d-122"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="62f7d-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="62f7d-123">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="62f7d-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="62f7d-124">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="62f7d-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="62f7d-125">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="62f7d-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="62f7d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="62f7d-126">Requirements</span></span>



| <span data-ttu-id="62f7d-127">需求</span><span class="sxs-lookup"><span data-stu-id="62f7d-127">Requirement</span></span> | <span data-ttu-id="62f7d-128">值</span><span class="sxs-lookup"><span data-stu-id="62f7d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62f7d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62f7d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62f7d-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="62f7d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62f7d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62f7d-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62f7d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62f7d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="62f7d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f7d-134"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="62f7d-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f7d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62f7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f7d-136">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="62f7d-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
