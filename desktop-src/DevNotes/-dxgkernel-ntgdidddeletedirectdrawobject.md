---
description: 終結先前建立的核心模式 Microsoft DirectDraw 裝置物件。
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: 'NtGdiDdDeleteDirectDrawObject 函式 (Ntgdi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110125"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="ea56d-103">NtGdiDdDeleteDirectDrawObject 函式</span><span class="sxs-lookup"><span data-stu-id="ea56d-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="ea56d-104">\[這項功能可能會隨著每個作業系統修訂而變更。</span><span class="sxs-lookup"><span data-stu-id="ea56d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ea56d-105">相反地，請使用 DirectDraw 和 Microsoft Direct3DAPIs;這些 Api 會防止應用程式進行這類作業系統變更，並隱藏與顯示驅動程式直接互動的許多其他難題。\]</span><span class="sxs-lookup"><span data-stu-id="ea56d-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ea56d-106">終結先前建立的核心模式 Microsoft DirectDraw 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="ea56d-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea56d-107">語法</span><span class="sxs-lookup"><span data-stu-id="ea56d-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="ea56d-108">參數</span><span class="sxs-lookup"><span data-stu-id="ea56d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea56d-109">*hDirectDrawLocal*</span><span class="sxs-lookup"><span data-stu-id="ea56d-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="ea56d-110">核心模式 DirectDraw 裝置物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ea56d-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea56d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea56d-111">Return value</span></span>

<span data-ttu-id="ea56d-112">如果成功，此函式會傳回 **TRUE**;否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ea56d-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea56d-113">備註</span><span class="sxs-lookup"><span data-stu-id="ea56d-113">Remarks</span></span>

<span data-ttu-id="ea56d-114">建議應用程式使用 DirectDraw 和 [Direct3D](../direct3d10/d3d10-graphics-reference.md) api 來建立和管理圖形裝置物件。</span><span class="sxs-lookup"><span data-stu-id="ea56d-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="ea56d-115">這些結構以簡化與作業系統無關的方式來抽象化裝置建立程式。</span><span class="sxs-lookup"><span data-stu-id="ea56d-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea56d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea56d-116">Requirements</span></span>



| <span data-ttu-id="ea56d-117">需求</span><span class="sxs-lookup"><span data-stu-id="ea56d-117">Requirement</span></span> | <span data-ttu-id="ea56d-118">值</span><span class="sxs-lookup"><span data-stu-id="ea56d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea56d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea56d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea56d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea56d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ea56d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea56d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea56d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea56d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea56d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ea56d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea56d-124"><dt>Ntgdi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea56d-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea56d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea56d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea56d-126">圖形低層級用戶端支援</span><span class="sxs-lookup"><span data-stu-id="ea56d-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="ea56d-127">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="ea56d-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="ea56d-128">**DdDeleteDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="ea56d-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
