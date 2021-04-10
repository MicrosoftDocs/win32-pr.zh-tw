---
title: 'TVM_MAPHTREEITEMTOACCID 訊息 (Commctrl .h) '
description: 將 HTREEITEM 對應至存取範圍識別碼。
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103721"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="9bad1-104">TVM \_ MAPHTREEITEMTOACCID 訊息</span><span class="sxs-lookup"><span data-stu-id="9bad1-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="9bad1-105">將 **HTREEITEM** 對應至存取範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bad1-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bad1-106">參數</span><span class="sxs-lookup"><span data-stu-id="9bad1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bad1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bad1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9bad1-108">對應至存取範圍識別碼的 **HTREEITEM** 。</span><span class="sxs-lookup"><span data-stu-id="9bad1-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="9bad1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bad1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9bad1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9bad1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bad1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bad1-111">Return value</span></span>

<span data-ttu-id="9bad1-112">傳回存取範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bad1-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bad1-113">備註</span><span class="sxs-lookup"><span data-stu-id="9bad1-113">Remarks</span></span>

<span data-ttu-id="9bad1-114">當您將專案加入至樹狀檢視控制項時，會傳回可唯一識別該專案的 **HTREEITEM** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bad1-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="9bad1-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="9bad1-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9bad1-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9bad1-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9bad1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bad1-117">Requirements</span></span>



| <span data-ttu-id="9bad1-118">需求</span><span class="sxs-lookup"><span data-stu-id="9bad1-118">Requirement</span></span> | <span data-ttu-id="9bad1-119">值</span><span class="sxs-lookup"><span data-stu-id="9bad1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bad1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bad1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9bad1-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bad1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bad1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bad1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9bad1-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bad1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bad1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9bad1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bad1-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9bad1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bad1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bad1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bad1-127">**TreeView \_ MapHTREEITEMtoAccID**</span><span class="sxs-lookup"><span data-stu-id="9bad1-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





