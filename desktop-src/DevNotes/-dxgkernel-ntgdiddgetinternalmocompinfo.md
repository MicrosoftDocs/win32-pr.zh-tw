---
description: 允許驅動程式報告它會在內部配置顯示記憶體，以執行動作補償。
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: 'NtGdiDdGetInternalMoCompInfo 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a9ddbb7843c7a1142ac6cd9906ef1ed3265e5d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847275"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a><span data-ttu-id="1aa30-103">NtGdiDdGetInternalMoCompInfo 函式</span><span class="sxs-lookup"><span data-stu-id="1aa30-103">NtGdiDdGetInternalMoCompInfo function</span></span>

<span data-ttu-id="1aa30-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="1aa30-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1aa30-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="1aa30-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1aa30-106">允許驅動程式報告它會在內部配置顯示記憶體，以執行動作補償。</span><span class="sxs-lookup"><span data-stu-id="1aa30-106">Allows the driver to report that it internally allocates display memory to perform motion compensation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa30-107">語法</span><span class="sxs-lookup"><span data-stu-id="1aa30-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a><span data-ttu-id="1aa30-108">參數</span><span class="sxs-lookup"><span data-stu-id="1aa30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa30-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aa30-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa30-110">先前建立之核心模式 DirectDraw 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1aa30-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="1aa30-111">*puGetInternalData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1aa30-111">*puGetInternalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa30-112">包含內部記憶體需求之 [**DD \_ GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1aa30-112">Pointer to a [**DD\_GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) structure that contains the internal memory requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa30-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1aa30-113">Return value</span></span>

<span data-ttu-id="1aa30-114">**NtGdiDdGetInternalMoCompInfo** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="1aa30-114">**NtGdiDdGetInternalMoCompInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1aa30-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1aa30-115">Return code</span></span>                                                                                              | <span data-ttu-id="1aa30-116">Description</span><span class="sxs-lookup"><span data-stu-id="1aa30-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1aa30-117"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="1aa30-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1aa30-118">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1aa30-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1aa30-119">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="1aa30-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1aa30-120">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="1aa30-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1aa30-121"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="1aa30-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1aa30-122">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="1aa30-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1aa30-123">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="1aa30-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1aa30-124">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="1aa30-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1aa30-125">備註</span><span class="sxs-lookup"><span data-stu-id="1aa30-125">Remarks</span></span>

<span data-ttu-id="1aa30-126">如需詳細資訊，請參閱 Microsoft (DDK) 的 Microsoft DirectX 影片加速驅動程式開發工具組。</span><span class="sxs-lookup"><span data-stu-id="1aa30-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa30-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aa30-127">Requirements</span></span>



| <span data-ttu-id="1aa30-128">需求</span><span class="sxs-lookup"><span data-stu-id="1aa30-128">Requirement</span></span> | <span data-ttu-id="1aa30-129">值</span><span class="sxs-lookup"><span data-stu-id="1aa30-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa30-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aa30-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa30-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aa30-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1aa30-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aa30-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa30-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aa30-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1aa30-134">標頭</span><span class="sxs-lookup"><span data-stu-id="1aa30-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aa30-135"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa30-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa30-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aa30-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa30-137">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="1aa30-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
