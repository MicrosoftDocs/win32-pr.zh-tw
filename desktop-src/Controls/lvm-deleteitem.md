---
title: 'LVM_DELETEITEM 訊息 (Commctrl .h) '
description: 從清單視圖控制項中移除專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteItem 宏來傳送。
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093852"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="a2a86-105">LVM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="a2a86-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="a2a86-106">從清單視圖控制項中移除專案。</span><span class="sxs-lookup"><span data-stu-id="a2a86-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="a2a86-107">您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="a2a86-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2a86-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2a86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a86-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2a86-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2a86-110">要刪除之清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="a2a86-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="a2a86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2a86-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a2a86-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a2a86-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a86-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2a86-113">Return value</span></span>

<span data-ttu-id="a2a86-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a2a86-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a86-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2a86-115">Requirements</span></span>



| <span data-ttu-id="a2a86-116">需求</span><span class="sxs-lookup"><span data-stu-id="a2a86-116">Requirement</span></span> | <span data-ttu-id="a2a86-117">值</span><span class="sxs-lookup"><span data-stu-id="a2a86-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a86-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2a86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a86-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2a86-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2a86-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2a86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a86-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2a86-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2a86-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a2a86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a86-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a86-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





