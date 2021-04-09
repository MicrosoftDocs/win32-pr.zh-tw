---
description: 設定裝置的 gamma 斜坡。
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: 'NtGdiDdSetGammaRamp 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110121"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="3b983-103">NtGdiDdSetGammaRamp 函式</span><span class="sxs-lookup"><span data-stu-id="3b983-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="3b983-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="3b983-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="3b983-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="3b983-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="3b983-106">設定裝置的 gamma 斜坡。</span><span class="sxs-lookup"><span data-stu-id="3b983-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b983-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b983-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="3b983-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b983-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b983-109">*hDirectDraw* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b983-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b983-110">要設定其曲線之核心模式驅動程式物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b983-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="3b983-111">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b983-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b983-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="3b983-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3b983-113">*lpGammaRamp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b983-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b983-114">**DDGAMMARAMP** 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="3b983-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b983-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b983-115">Return value</span></span>

<span data-ttu-id="3b983-116">如果函式成功，則傳回值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3b983-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="3b983-117">否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3b983-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b983-118">備註</span><span class="sxs-lookup"><span data-stu-id="3b983-118">Remarks</span></span>

<span data-ttu-id="3b983-119">建議應用程式改為使用 **IDirectDrawGammaControl：： SetGammaRamp** 或 [**IDirect3DDevice9：： SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 方法，因為這些方法提供的功能與作業系統無關。</span><span class="sxs-lookup"><span data-stu-id="3b983-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b983-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b983-120">Requirements</span></span>



| <span data-ttu-id="3b983-121">需求</span><span class="sxs-lookup"><span data-stu-id="3b983-121">Requirement</span></span> | <span data-ttu-id="3b983-122">值</span><span class="sxs-lookup"><span data-stu-id="3b983-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b983-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b983-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b983-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b983-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3b983-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b983-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b983-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b983-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3b983-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3b983-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b983-128"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b983-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b983-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b983-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b983-130">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="3b983-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
