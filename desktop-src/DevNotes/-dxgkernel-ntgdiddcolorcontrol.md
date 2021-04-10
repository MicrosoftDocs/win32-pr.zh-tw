---
description: 控制重迭表面的亮度和亮度控制項。
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: 'NtGdiDdColorControl 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45ed8683a892b07fa63fbe79b657669e647126cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110137"
---
# <a name="ntgdiddcolorcontrol-function"></a><span data-ttu-id="19632-103">NtGdiDdColorControl 函式</span><span class="sxs-lookup"><span data-stu-id="19632-103">NtGdiDdColorControl function</span></span>

<span data-ttu-id="19632-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="19632-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="19632-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="19632-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="19632-106">控制重迭表面的亮度和亮度控制項。</span><span class="sxs-lookup"><span data-stu-id="19632-106">Controls the luminance and brightness controls of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="19632-107">語法</span><span class="sxs-lookup"><span data-stu-id="19632-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a><span data-ttu-id="19632-108">參數</span><span class="sxs-lookup"><span data-stu-id="19632-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19632-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19632-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19632-110">代表重迭表面之 [**DD \_ 介面 \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="19632-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="19632-111">*puColorControlData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="19632-111">*puColorControlData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19632-112">[**DD \_ COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata)結構的指標，其中包含指定之重迭表面的色彩控制項資訊。</span><span class="sxs-lookup"><span data-stu-id="19632-112">Pointer to a [**DD\_COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) structure that contains the color control information for a specified overlay surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19632-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="19632-113">Return value</span></span>

<span data-ttu-id="19632-114">**NtGdiDdColorControl** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="19632-114">**NtGdiDdColorControl** returns one of the following callback codes.</span></span>



| <span data-ttu-id="19632-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="19632-115">Return code</span></span>                                                                                              | <span data-ttu-id="19632-116">Description</span><span class="sxs-lookup"><span data-stu-id="19632-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19632-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="19632-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="19632-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="19632-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="19632-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="19632-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="19632-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="19632-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="19632-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="19632-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="19632-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="19632-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="19632-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="19632-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="19632-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="19632-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19632-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="19632-125">Requirements</span></span>



| <span data-ttu-id="19632-126">需求</span><span class="sxs-lookup"><span data-stu-id="19632-126">Requirement</span></span> | <span data-ttu-id="19632-127">值</span><span class="sxs-lookup"><span data-stu-id="19632-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19632-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19632-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19632-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19632-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="19632-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19632-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19632-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19632-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19632-132">標頭</span><span class="sxs-lookup"><span data-stu-id="19632-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19632-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="19632-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19632-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19632-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19632-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="19632-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
