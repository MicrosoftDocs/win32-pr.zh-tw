---
description: 在模式切換之後，重新啟用 Microsoft DirectDraw 核心模式裝置物件。
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: 'NtGdiDdReenableDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111168"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="d4098-103">NtGdiDdReenableDirectDrawObject 函式</span><span class="sxs-lookup"><span data-stu-id="d4098-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="d4098-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="d4098-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d4098-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="d4098-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d4098-106">在模式切換之後，重新啟用 Microsoft DirectDraw 核心模式裝置物件。</span><span class="sxs-lookup"><span data-stu-id="d4098-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4098-107">語法</span><span class="sxs-lookup"><span data-stu-id="d4098-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="d4098-108">參數</span><span class="sxs-lookup"><span data-stu-id="d4098-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4098-109">*hDirectDrawLocal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4098-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4098-110">需要重新啟用的 DirectDraw 物件。</span><span class="sxs-lookup"><span data-stu-id="d4098-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d4098-111">*pubNewMode* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d4098-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4098-112">BOOL 的指標，將會填入表示顯示模式是否已變更的值。</span><span class="sxs-lookup"><span data-stu-id="d4098-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4098-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4098-113">Return value</span></span>

<span data-ttu-id="d4098-114">如果成功 (可以重新啟用裝置) ，此函式會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d4098-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="d4098-115">否則 (例如，顯示驅動程式已變更) ，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d4098-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4098-116">備註</span><span class="sxs-lookup"><span data-stu-id="d4098-116">Remarks</span></span>

<span data-ttu-id="d4098-117">重新啟用物件之後，就可以透過呼叫 [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md)來重新查詢裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="d4098-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="d4098-118">建議應用程式使用 DirectDraw 或 [Direct3D](../direct3d10/d3d10-graphics-reference.md) 8 版的 api，以與作業系統無關的方式將此程式自動化及抽象化。</span><span class="sxs-lookup"><span data-stu-id="d4098-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4098-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4098-119">Requirements</span></span>



| <span data-ttu-id="d4098-120">需求</span><span class="sxs-lookup"><span data-stu-id="d4098-120">Requirement</span></span> | <span data-ttu-id="d4098-121">值</span><span class="sxs-lookup"><span data-stu-id="d4098-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4098-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4098-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4098-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4098-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d4098-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4098-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4098-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4098-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4098-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d4098-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4098-127"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4098-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4098-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4098-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4098-129">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="d4098-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="d4098-130">**DdReenableDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="d4098-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
