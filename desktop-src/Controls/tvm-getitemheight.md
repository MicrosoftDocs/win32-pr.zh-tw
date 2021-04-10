---
title: 'TVM_GETITEMHEIGHT 訊息 (Commctrl .h) '
description: 抓取每個樹狀檢視專案目前的高度。 您可以使用 TreeView GetItemHeight 宏明確地傳送此訊息 \_ 。
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844435"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="eb8af-105">TVM \_ GETITEMHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="eb8af-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="eb8af-106">抓取每個樹狀檢視專案目前的高度。</span><span class="sxs-lookup"><span data-stu-id="eb8af-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="eb8af-107">您可以使用 [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="eb8af-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb8af-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb8af-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb8af-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb8af-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eb8af-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb8af-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb8af-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb8af-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eb8af-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb8af-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb8af-113">Return value</span></span>

<span data-ttu-id="eb8af-114">傳回每個專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb8af-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8af-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb8af-115">Requirements</span></span>



| <span data-ttu-id="eb8af-116">需求</span><span class="sxs-lookup"><span data-stu-id="eb8af-116">Requirement</span></span> | <span data-ttu-id="eb8af-117">值</span><span class="sxs-lookup"><span data-stu-id="eb8af-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8af-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb8af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8af-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb8af-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb8af-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb8af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8af-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb8af-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb8af-122">標頭</span><span class="sxs-lookup"><span data-stu-id="eb8af-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb8af-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb8af-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb8af-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb8af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8af-125">**TVM \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="eb8af-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





