---
title: 'TVM_MAPACCIDTOHTREEITEM 訊息 (Commctrl .h) '
description: 將存取範圍識別碼對應至 HTREEITEM。
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024834"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="c6ad2-104">TVM \_ MAPACCIDTOHTREEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="c6ad2-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="c6ad2-105">將存取範圍識別碼對應至 **HTREEITEM**。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6ad2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ad2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6ad2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c6ad2-108">包含要對應至 **HTREEITEM** 之存取範圍識別碼的 **UINT** 。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="c6ad2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6ad2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c6ad2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ad2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6ad2-111">Return value</span></span>

<span data-ttu-id="c6ad2-112">傳回指定的協助工具識別碼所對應的 **HTREEITEM** 。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ad2-113">備註</span><span class="sxs-lookup"><span data-stu-id="c6ad2-113">Remarks</span></span>

<span data-ttu-id="c6ad2-114">當您將專案加入至樹狀檢視控制項時， **HTREEITEM** 會傳回可唯一識別該專案的。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="c6ad2-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c6ad2-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c6ad2-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6ad2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6ad2-117">Requirements</span></span>



| <span data-ttu-id="c6ad2-118">需求</span><span class="sxs-lookup"><span data-stu-id="c6ad2-118">Requirement</span></span> | <span data-ttu-id="c6ad2-119">值</span><span class="sxs-lookup"><span data-stu-id="c6ad2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ad2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6ad2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ad2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6ad2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6ad2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6ad2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ad2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6ad2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6ad2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c6ad2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ad2-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ad2-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ad2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6ad2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ad2-127">**TreeView \_ MapAccIDToHTREEITEM**</span><span class="sxs-lookup"><span data-stu-id="c6ad2-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





