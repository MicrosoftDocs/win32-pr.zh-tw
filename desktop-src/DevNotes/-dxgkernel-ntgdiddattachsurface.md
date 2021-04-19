---
description: 附加兩個核心模式介面表示。
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: 'NtGdiDdAttachSurface 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970309"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="5f0d7-103">NtGdiDdAttachSurface 函式</span><span class="sxs-lookup"><span data-stu-id="5f0d7-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="5f0d7-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5f0d7-105">請改用 Microsoft DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="5f0d7-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5f0d7-106">附加兩個核心模式介面表示。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0d7-107">語法</span><span class="sxs-lookup"><span data-stu-id="5f0d7-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="5f0d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f0d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0d7-109">*hSurfaceFrom* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f0d7-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0d7-110">核心模式介面物件的控制碼，該物件將會成為新附件的起點。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="5f0d7-111">*hSurfaceTo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f0d7-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0d7-112">核心模式介面物件的控制碼，該物件將會成為新附件的結束點。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0d7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f0d7-113">Return value</span></span>

<span data-ttu-id="5f0d7-114">**NtGdiDdAttachSurface** 會傳回下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="5f0d7-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="5f0d7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5f0d7-115">Return code</span></span>                                                                          | <span data-ttu-id="5f0d7-116">Description</span><span class="sxs-lookup"><span data-stu-id="5f0d7-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="5f0d7-117"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0d7-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="5f0d7-118">函式呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="5f0d7-119"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="5f0d7-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="5f0d7-120">函式呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="5f0d7-121">備註</span><span class="sxs-lookup"><span data-stu-id="5f0d7-121">Remarks</span></span>

<span data-ttu-id="5f0d7-122">請參閱 DirectDraw 軟體發展工具組 (SDK) 和驅動程式開發工具組 (DDK) 以取得 surface 附件的完整描述。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="5f0d7-123">如同其他介面附件，所產生的附件是單向的。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="5f0d7-124">呼叫此函式之後， *hSurfaceTo* 將不會附加至 *hSurfaceFrom*。</span><span class="sxs-lookup"><span data-stu-id="5f0d7-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f0d7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f0d7-125">Requirements</span></span>



| <span data-ttu-id="5f0d7-126">需求</span><span class="sxs-lookup"><span data-stu-id="5f0d7-126">Requirement</span></span> | <span data-ttu-id="5f0d7-127">值</span><span class="sxs-lookup"><span data-stu-id="5f0d7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0d7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f0d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0d7-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f0d7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5f0d7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f0d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0d7-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f0d7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f0d7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5f0d7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0d7-133"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0d7-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0d7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f0d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0d7-135">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="5f0d7-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




