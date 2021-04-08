---
description: 終結先前配置的核心模式 Microsoft DirectDraw 介面物件，該物件是使用設定為 DDSCAPS EXECUTEBUFFER 之 DDSCAPS 結構的 dwCaps 成員所建立 \_ 。
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: 'NtGdiDdDestroyD3DBuffer 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688536"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="a90a6-103">NtGdiDdDestroyD3DBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="a90a6-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="a90a6-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="a90a6-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a90a6-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="a90a6-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a90a6-106">終結先前配置的核心模式 Microsoft DirectDraw 介面物件，該物件是使用設定為 DDSCAPS EXECUTEBUFFER 之 [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85))結構的 **dwCaps** 成員所建立 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a90a6-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90a6-107">語法</span><span class="sxs-lookup"><span data-stu-id="a90a6-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="a90a6-108">參數</span><span class="sxs-lookup"><span data-stu-id="a90a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90a6-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a90a6-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90a6-110">[**DD \_ DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata)結構的控制碼，其中包含損毀 Direct3D 命令或頂點緩衝區所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="a90a6-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90a6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a90a6-111">Return value</span></span>

<span data-ttu-id="a90a6-112">**NtGdiDdDestroyD3DBuffer** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="a90a6-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a90a6-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a90a6-113">Return code</span></span>                                                                                              | <span data-ttu-id="a90a6-114">Description</span><span class="sxs-lookup"><span data-stu-id="a90a6-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a90a6-115"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="a90a6-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a90a6-116">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a90a6-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a90a6-117">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="a90a6-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a90a6-118">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="a90a6-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a90a6-119"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="a90a6-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a90a6-120">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="a90a6-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a90a6-121">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="a90a6-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a90a6-122">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="a90a6-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a90a6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a90a6-123">Requirements</span></span>



| <span data-ttu-id="a90a6-124">需求</span><span class="sxs-lookup"><span data-stu-id="a90a6-124">Requirement</span></span> | <span data-ttu-id="a90a6-125">值</span><span class="sxs-lookup"><span data-stu-id="a90a6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a90a6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a90a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a90a6-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a90a6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a90a6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a90a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a90a6-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a90a6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a90a6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a90a6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a90a6-131"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a90a6-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a90a6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a90a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90a6-133">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="a90a6-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
