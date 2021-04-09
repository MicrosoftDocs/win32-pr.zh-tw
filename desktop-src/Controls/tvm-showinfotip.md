---
title: 'TVM_SHOWINFOTIP 訊息 (Commctrl .h) '
description: 顯示樹狀檢視控制項中所指定專案的提示。 您可以明確地傳送此訊息，或使用 TreeView \_ ShowInfoTip 宏來傳送。
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844363"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="c0a88-105">TVM \_ SHOWINFOTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="c0a88-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="c0a88-106">顯示樹狀檢視控制項中所指定專案的提示。</span><span class="sxs-lookup"><span data-stu-id="c0a88-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="c0a88-107">您可以明確地傳送此訊息，或使用 [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="c0a88-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="c0a88-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0a88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0a88-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0a88-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c0a88-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c0a88-111">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0a88-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a88-112">專案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c0a88-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a88-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0a88-113">Return value</span></span>

<span data-ttu-id="c0a88-114">傳回零。</span><span class="sxs-lookup"><span data-stu-id="c0a88-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0a88-115">備註</span><span class="sxs-lookup"><span data-stu-id="c0a88-115">Remarks</span></span>

<span data-ttu-id="c0a88-116">大部分的應用程式都不會使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="c0a88-116">Most applications do not use this message.</span></span> <span data-ttu-id="c0a88-117">提示會自動顯示。</span><span class="sxs-lookup"><span data-stu-id="c0a88-117">Infotips are shown automatically.</span></span> <span data-ttu-id="c0a88-118">如需詳細資訊，請參閱 [關於 Tree-View 控制項](tree-view-controls.md) 總覽中的使用樹狀檢視提示。</span><span class="sxs-lookup"><span data-stu-id="c0a88-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a88-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0a88-119">Requirements</span></span>



| <span data-ttu-id="c0a88-120">需求</span><span class="sxs-lookup"><span data-stu-id="c0a88-120">Requirement</span></span> | <span data-ttu-id="c0a88-121">值</span><span class="sxs-lookup"><span data-stu-id="c0a88-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a88-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0a88-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a88-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0a88-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0a88-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0a88-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a88-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0a88-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0a88-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c0a88-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0a88-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a88-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





