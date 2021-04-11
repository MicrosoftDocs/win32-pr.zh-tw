---
description: 允許驅動程式指定支援指定的 GUID 所需的過渡表面數量，以及這些介面每個表面的大小、位置和格式。
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: 'NtGdiDdGetMoCompBuffInfo 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03d471e62edd061ce167e0baf2051836e9634fae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025911"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a><span data-ttu-id="d1d2b-103">NtGdiDdGetMoCompBuffInfo 函式</span><span class="sxs-lookup"><span data-stu-id="d1d2b-103">NtGdiDdGetMoCompBuffInfo function</span></span>

<span data-ttu-id="d1d2b-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d1d2b-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="d1d2b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d1d2b-106">允許驅動程式指定支援指定的 GUID 所需的過渡表面數量，以及這些介面每個表面的大小、位置和格式。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-106">Allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d2b-107">語法</span><span class="sxs-lookup"><span data-stu-id="d1d2b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a><span data-ttu-id="d1d2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="d1d2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d2b-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1d2b-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d2b-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="d1d2b-111">*puGetBuffData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d1d2b-111">*puGetBuffData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d2b-112">[**DD \_ GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata)結構的指標，其中包含壓縮的緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-112">Pointer to a [**DD\_GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) structure that contains the compressed buffer information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1d2b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1d2b-113">Return value</span></span>

<span data-ttu-id="d1d2b-114">**NtGdiDdGetMoCompBuffInfo** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-114">**NtGdiDdGetMoCompBuffInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d1d2b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d1d2b-115">Return code</span></span>                                                                                              | <span data-ttu-id="d1d2b-116">Description</span><span class="sxs-lookup"><span data-stu-id="d1d2b-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1d2b-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d2b-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d1d2b-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d1d2b-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d1d2b-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d1d2b-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="d1d2b-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d1d2b-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d1d2b-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d1d2b-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1d2b-125">備註</span><span class="sxs-lookup"><span data-stu-id="d1d2b-125">Remarks</span></span>

<span data-ttu-id="d1d2b-126">如需詳細資訊，請參閱 Microsoft (DDK) 的 Microsoft DirectX 影片加速驅動程式開發工具組。</span><span class="sxs-lookup"><span data-stu-id="d1d2b-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d2b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1d2b-127">Requirements</span></span>



| <span data-ttu-id="d1d2b-128">需求</span><span class="sxs-lookup"><span data-stu-id="d1d2b-128">Requirement</span></span> | <span data-ttu-id="d1d2b-129">值</span><span class="sxs-lookup"><span data-stu-id="d1d2b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d2b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1d2b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d2b-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1d2b-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d1d2b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1d2b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d2b-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1d2b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1d2b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d1d2b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d2b-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d2b-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d2b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1d2b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d2b-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="d1d2b-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
