---
title: 'HDM_GETITEMCOUNT 訊息 (Commctrl .h) '
description: 取得標題控制項中的專案計數。 您可以明確地傳送此訊息，或使用標頭 \_ GetItemCount 宏。
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104484"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="10483-105">HDM \_ GETITEMCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="10483-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="10483-106">取得標題控制項中的專案計數。</span><span class="sxs-lookup"><span data-stu-id="10483-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="10483-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) 宏。</span><span class="sxs-lookup"><span data-stu-id="10483-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10483-108">參數</span><span class="sxs-lookup"><span data-stu-id="10483-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10483-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10483-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10483-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="10483-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10483-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10483-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10483-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="10483-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10483-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="10483-113">Return value</span></span>

<span data-ttu-id="10483-114">如果成功，則傳回專案的數目，否則為-1。</span><span class="sxs-lookup"><span data-stu-id="10483-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="10483-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10483-115">Requirements</span></span>



| <span data-ttu-id="10483-116">需求</span><span class="sxs-lookup"><span data-stu-id="10483-116">Requirement</span></span> | <span data-ttu-id="10483-117">值</span><span class="sxs-lookup"><span data-stu-id="10483-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10483-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10483-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10483-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10483-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10483-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10483-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10483-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10483-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10483-122">標頭</span><span class="sxs-lookup"><span data-stu-id="10483-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10483-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="10483-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





