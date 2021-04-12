---
title: 'LVM_DELETEALLITEMS 訊息 (Commctrl .h) '
description: 移除清單視圖控制項中的所有專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteAllItems 宏來傳送。
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464297"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="16464-105">LVM \_ DELETEALLITEMS 訊息</span><span class="sxs-lookup"><span data-stu-id="16464-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="16464-106">移除清單視圖控制項中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="16464-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="16464-107">您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="16464-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="16464-108">參數</span><span class="sxs-lookup"><span data-stu-id="16464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16464-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16464-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="16464-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="16464-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="16464-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16464-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="16464-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="16464-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16464-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="16464-113">Return value</span></span>

<span data-ttu-id="16464-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="16464-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16464-115">備註</span><span class="sxs-lookup"><span data-stu-id="16464-115">Remarks</span></span>

<span data-ttu-id="16464-116">當清單視圖控制項收到 **LVM \_ DELETEALLITEMS** 訊息時，它會將 [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) 通知程式碼傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="16464-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="16464-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="16464-117">Requirements</span></span>



| <span data-ttu-id="16464-118">需求</span><span class="sxs-lookup"><span data-stu-id="16464-118">Requirement</span></span> | <span data-ttu-id="16464-119">值</span><span class="sxs-lookup"><span data-stu-id="16464-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16464-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16464-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16464-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16464-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16464-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16464-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16464-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16464-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16464-124">標頭</span><span class="sxs-lookup"><span data-stu-id="16464-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16464-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="16464-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





