---
description: 建立 Microsoft DirectDraw 物件的核心端標記法。
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: 'NtGdiDdCreateDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110129"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="ff065-103">NtGdiDdCreateDirectDrawObject 函式</span><span class="sxs-lookup"><span data-stu-id="ff065-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="ff065-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="ff065-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ff065-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="ff065-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ff065-106">建立 Microsoft DirectDraw 物件的核心端標記法。</span><span class="sxs-lookup"><span data-stu-id="ff065-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff065-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff065-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="ff065-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff065-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff065-109">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff065-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff065-110">應建立 DirectDraw 物件的任何 DC 顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="ff065-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff065-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff065-111">Return value</span></span>

<span data-ttu-id="ff065-112">如果成功，此函式會傳回核心模式物件表示的控制碼;否則，它會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ff065-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff065-113">備註</span><span class="sxs-lookup"><span data-stu-id="ff065-113">Remarks</span></span>

<span data-ttu-id="ff065-114">建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。</span><span class="sxs-lookup"><span data-stu-id="ff065-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="ff065-115">這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。</span><span class="sxs-lookup"><span data-stu-id="ff065-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff065-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff065-116">Requirements</span></span>



| <span data-ttu-id="ff065-117">需求</span><span class="sxs-lookup"><span data-stu-id="ff065-117">Requirement</span></span> | <span data-ttu-id="ff065-118">值</span><span class="sxs-lookup"><span data-stu-id="ff065-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff065-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff065-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff065-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff065-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ff065-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff065-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff065-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff065-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff065-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ff065-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff065-124"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff065-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff065-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff065-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff065-126">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="ff065-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="ff065-127">**DdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="ff065-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
