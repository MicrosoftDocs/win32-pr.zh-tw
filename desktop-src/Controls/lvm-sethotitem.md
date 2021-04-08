---
title: 'LVM_SETHOTITEM 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的熱專案。 您可以明確地傳送此訊息，或使用 ListView \_ SetHotItem 宏。
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685518"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="042c8-105">LVM \_ SETHOTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="042c8-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="042c8-106">設定清單視圖控制項的熱專案。</span><span class="sxs-lookup"><span data-stu-id="042c8-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="042c8-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="042c8-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="042c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="042c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="042c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="042c8-110">以零為基底的索引，這是要設定為熱專案的專案。</span><span class="sxs-lookup"><span data-stu-id="042c8-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="042c8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="042c8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="042c8-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="042c8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042c8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="042c8-113">Return value</span></span>

<span data-ttu-id="042c8-114">傳回先前熱的專案索引。</span><span class="sxs-lookup"><span data-stu-id="042c8-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="042c8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="042c8-115">Requirements</span></span>



| <span data-ttu-id="042c8-116">需求</span><span class="sxs-lookup"><span data-stu-id="042c8-116">Requirement</span></span> | <span data-ttu-id="042c8-117">值</span><span class="sxs-lookup"><span data-stu-id="042c8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="042c8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="042c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="042c8-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="042c8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="042c8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="042c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="042c8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="042c8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="042c8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="042c8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="042c8-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="042c8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





