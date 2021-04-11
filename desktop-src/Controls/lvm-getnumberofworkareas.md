---
title: 'LVM_GETNUMBEROFWORKAREAS 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中的工作區數目。 您可以明確地傳送此訊息，或使用 ListView \_ GetNumberOfWorkAreas 宏。
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934895"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="c2a34-105">LVM \_ GETNUMBEROFWORKAREAS 訊息</span><span class="sxs-lookup"><span data-stu-id="c2a34-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="c2a34-106">抓取清單視圖控制項中的工作區數目。</span><span class="sxs-lookup"><span data-stu-id="c2a34-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="c2a34-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) 宏。</span><span class="sxs-lookup"><span data-stu-id="c2a34-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2a34-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2a34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a34-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2a34-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2a34-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c2a34-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2a34-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2a34-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a34-112">UINT 值的指標，此值會接收清單視圖控制項中的工作區數目。</span><span class="sxs-lookup"><span data-stu-id="c2a34-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="c2a34-113">如果在這個變數中放置零，則目前未設定任何工作區域。</span><span class="sxs-lookup"><span data-stu-id="c2a34-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="c2a34-114">此值不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c2a34-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a34-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2a34-115">Return value</span></span>

<span data-ttu-id="c2a34-116">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c2a34-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a34-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2a34-117">Requirements</span></span>



| <span data-ttu-id="c2a34-118">需求</span><span class="sxs-lookup"><span data-stu-id="c2a34-118">Requirement</span></span> | <span data-ttu-id="c2a34-119">值</span><span class="sxs-lookup"><span data-stu-id="c2a34-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a34-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2a34-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a34-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a34-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2a34-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2a34-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a34-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a34-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2a34-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c2a34-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a34-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a34-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a34-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2a34-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a34-127">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="c2a34-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





