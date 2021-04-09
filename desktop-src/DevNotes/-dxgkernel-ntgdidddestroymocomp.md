---
description: 通知驅動程式，將不會再使用這個動作補償物件。 驅動程式現在需要執行任何必要的清除。
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: 'NtGdiDdDestroyMoComp 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847189"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="9a926-104">NtGdiDdDestroyMoComp 函式</span><span class="sxs-lookup"><span data-stu-id="9a926-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="9a926-105">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="9a926-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9a926-106">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="9a926-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9a926-107">通知驅動程式，將不會再使用這個動作補償物件。</span><span class="sxs-lookup"><span data-stu-id="9a926-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="9a926-108">驅動程式現在需要執行任何必要的清除。</span><span class="sxs-lookup"><span data-stu-id="9a926-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a926-109">語法</span><span class="sxs-lookup"><span data-stu-id="9a926-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="9a926-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a926-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a926-111">*hMoComp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a926-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a926-112">[**DD \_ MOTIONCOMP \_ 區域**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local)結構的控制碼，其中包含要終結之動作補償物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9a926-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="9a926-113">*puBeginFrameData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9a926-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a926-114">[**DD \_ DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata)結構的指標，其中包含完成動作補償所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="9a926-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a926-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a926-115">Return value</span></span>

<span data-ttu-id="9a926-116">**NtGdiDdDestroyMoComp** 會傳回下列其中一個回呼碼。</span><span class="sxs-lookup"><span data-stu-id="9a926-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9a926-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a926-117">Return code</span></span>                                                                                              | <span data-ttu-id="9a926-118">Description</span><span class="sxs-lookup"><span data-stu-id="9a926-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a926-119"><dt>**DDHAL \_ 驅動程式已 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="9a926-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9a926-120">驅動程式已執行作業，並傳回該操作的有效傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9a926-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9a926-121">如果這個程式碼是 DD \_ OK，DirectDraw 或 Direct3D 會繼續執行函數。</span><span class="sxs-lookup"><span data-stu-id="9a926-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9a926-122">否則，DirectDraw 或 Direct3D 會傳回驅動程式所提供的錯誤碼，並中止函數。</span><span class="sxs-lookup"><span data-stu-id="9a926-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9a926-123"><dt>**DDHAL \_ 驅動程式 \_ NOTHANDLED**</dt></span><span class="sxs-lookup"><span data-stu-id="9a926-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9a926-124">驅動程式對要求的作業沒有任何批註。</span><span class="sxs-lookup"><span data-stu-id="9a926-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9a926-125">如果驅動程式必須執行特定的回呼，DirectDraw 或 Direct3D 會報告錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="9a926-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9a926-126">否則，DirectDraw 或 Direct3D 會處理此作業，就像尚未執行 DirectDraw 或 Direct3D 裝置獨立的執行所定義的驅動程式回呼一樣。</span><span class="sxs-lookup"><span data-stu-id="9a926-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a926-127">備註</span><span class="sxs-lookup"><span data-stu-id="9a926-127">Remarks</span></span>

<span data-ttu-id="9a926-128">如需詳細資訊，請參閱 Microsoft (DDK) 的 Microsoft DirectX 影片加速驅動程式開發工具組。</span><span class="sxs-lookup"><span data-stu-id="9a926-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a926-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a926-129">Requirements</span></span>



| <span data-ttu-id="9a926-130">需求</span><span class="sxs-lookup"><span data-stu-id="9a926-130">Requirement</span></span> | <span data-ttu-id="9a926-131">值</span><span class="sxs-lookup"><span data-stu-id="9a926-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a926-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a926-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a926-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a926-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9a926-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a926-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a926-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a926-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a926-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9a926-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a926-137"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a926-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a926-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a926-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a926-139">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="9a926-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
