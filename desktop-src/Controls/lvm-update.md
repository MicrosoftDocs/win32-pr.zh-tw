---
title: 'LVM_UPDATE 訊息 (Commctrl .h) '
description: 更新清單視圖專案。 如果清單視圖控制項有 LVS) \_ AUTOARRANGE 樣式，此宏就會排列清單視圖控制項。 您可以使用 ListView Update 宏明確地傳送此訊息 \_ 。
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843144"
---
# <a name="lvm_update-message"></a><span data-ttu-id="fc630-106">LVM \_ 更新訊息</span><span class="sxs-lookup"><span data-stu-id="fc630-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="fc630-107">更新清單視圖專案。</span><span class="sxs-lookup"><span data-stu-id="fc630-107">Updates a list-view item.</span></span> <span data-ttu-id="fc630-108">如果清單視圖控制項有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式，此宏就會排列清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="fc630-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="fc630-109">您可以使用 [**ListView \_ Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fc630-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc630-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc630-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc630-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc630-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc630-112">要更新之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="fc630-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="fc630-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc630-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fc630-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fc630-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc630-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc630-115">Return value</span></span>

<span data-ttu-id="fc630-116">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fc630-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc630-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc630-117">Requirements</span></span>



| <span data-ttu-id="fc630-118">需求</span><span class="sxs-lookup"><span data-stu-id="fc630-118">Requirement</span></span> | <span data-ttu-id="fc630-119">值</span><span class="sxs-lookup"><span data-stu-id="fc630-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc630-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc630-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fc630-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc630-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc630-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc630-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fc630-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc630-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc630-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fc630-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc630-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc630-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





