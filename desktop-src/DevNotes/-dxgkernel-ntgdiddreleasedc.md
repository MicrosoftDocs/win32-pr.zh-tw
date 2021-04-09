---
description: 針對指定的核心模式 Microsoft DirectDraw 介面物件，釋放先前建立的裝置內容 (DC) 。
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: 'NtGdiDdReleaseDC 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847032"
---
# <a name="ntgdiddreleasedc-function"></a><span data-ttu-id="bb2b4-103">NtGdiDdReleaseDC 函式</span><span class="sxs-lookup"><span data-stu-id="bb2b4-103">NtGdiDdReleaseDC function</span></span>

<span data-ttu-id="bb2b4-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="bb2b4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bb2b4-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="bb2b4-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bb2b4-106">針對指定的核心模式 Microsoft DirectDraw 介面物件，釋放先前建立的裝置內容 (DC) 。</span><span class="sxs-lookup"><span data-stu-id="bb2b4-106">Releases the previously created device context (DC) for the indicated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2b4-107">語法</span><span class="sxs-lookup"><span data-stu-id="bb2b4-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="bb2b4-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb2b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2b4-109">*hSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb2b4-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2b4-110">先前建立之核心模式 DirectDraw 介面物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bb2b4-110">Handle to the previously created kernel-mode DirectDraw surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2b4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb2b4-111">Return value</span></span>

<span data-ttu-id="bb2b4-112">如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bb2b4-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2b4-113">備註</span><span class="sxs-lookup"><span data-stu-id="bb2b4-113">Remarks</span></span>

<span data-ttu-id="bb2b4-114">需要取得 DirectDraw 介面之 DC 的應用程式可能會使用 [IDirectDrawSurface7：： GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc)，它會以與作業系統無關的方式來公開這項功能。</span><span class="sxs-lookup"><span data-stu-id="bb2b4-114">Applications that need to obtain a DC for a DirectDraw surface may use [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), which exposes this functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2b4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb2b4-115">Requirements</span></span>



| <span data-ttu-id="bb2b4-116">需求</span><span class="sxs-lookup"><span data-stu-id="bb2b4-116">Requirement</span></span> | <span data-ttu-id="bb2b4-117">值</span><span class="sxs-lookup"><span data-stu-id="bb2b4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2b4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb2b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2b4-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb2b4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb2b4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb2b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2b4-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb2b4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb2b4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bb2b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb2b4-123"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb2b4-123"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2b4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb2b4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2b4-125">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="bb2b4-125">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="bb2b4-126">**DdReleaseDC**</span><span class="sxs-lookup"><span data-stu-id="bb2b4-126">**DdReleaseDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
