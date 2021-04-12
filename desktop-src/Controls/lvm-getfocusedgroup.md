---
title: 'LVM_GETFOCUSEDGROUP 訊息 (Commctrl .h) '
description: 取得具有焦點的群組。 明確地傳送此訊息，或使用 ListView \_ GetFocusedGroup 宏。
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464273"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="a6352-105">LVM \_ GETFOCUSEDGROUP 訊息</span><span class="sxs-lookup"><span data-stu-id="a6352-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="a6352-106">取得具有焦點的群組。</span><span class="sxs-lookup"><span data-stu-id="a6352-106">Gets the group that has the focus.</span></span> <span data-ttu-id="a6352-107">明確地傳送此訊息，或使用 [**ListView \_ GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) 宏。</span><span class="sxs-lookup"><span data-stu-id="a6352-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6352-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6352-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6352-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6352-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a6352-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a6352-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a6352-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6352-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a6352-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a6352-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6352-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6352-113">Return value</span></span>

<span data-ttu-id="a6352-114">傳回狀態為 LVGS 之群組的索引 \_ ，如果沒有焦點在 LVGS 狀態的群組，則為-1 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a6352-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6352-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6352-115">Requirements</span></span>



| <span data-ttu-id="a6352-116">需求</span><span class="sxs-lookup"><span data-stu-id="a6352-116">Requirement</span></span> | <span data-ttu-id="a6352-117">值</span><span class="sxs-lookup"><span data-stu-id="a6352-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6352-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6352-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6352-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6352-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6352-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6352-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6352-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6352-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6352-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a6352-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6352-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6352-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





