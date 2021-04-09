---
title: 'LVM_SETCOLUMNORDERARRAY 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定資料行的由左到右的順序。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumnOrderArray 宏。
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024587"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="e5861-105">LVM \_ SETCOLUMNORDERARRAY 訊息</span><span class="sxs-lookup"><span data-stu-id="e5861-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="e5861-106">在清單視圖控制項中設定資料行的由左到右的順序。</span><span class="sxs-lookup"><span data-stu-id="e5861-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="e5861-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) 宏。</span><span class="sxs-lookup"><span data-stu-id="e5861-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5861-108">參數</span><span class="sxs-lookup"><span data-stu-id="e5861-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5861-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5861-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5861-110">緩衝區的大小（以元素為 *lParam*）。</span><span class="sxs-lookup"><span data-stu-id="e5861-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="e5861-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5861-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5861-112">陣列的指標，這個陣列會指定資料行的顯示順序（從左至右）。</span><span class="sxs-lookup"><span data-stu-id="e5861-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="e5861-113">例如，如果陣列的內容是 {2,0,1} ，控制項會依序顯示資料行2、資料行0和資料行1。</span><span class="sxs-lookup"><span data-stu-id="e5861-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5861-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5861-114">Return value</span></span>

<span data-ttu-id="e5861-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e5861-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5861-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5861-116">Requirements</span></span>



| <span data-ttu-id="e5861-117">需求</span><span class="sxs-lookup"><span data-stu-id="e5861-117">Requirement</span></span> | <span data-ttu-id="e5861-118">值</span><span class="sxs-lookup"><span data-stu-id="e5861-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5861-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5861-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5861-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5861-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5861-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5861-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5861-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5861-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5861-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e5861-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5861-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5861-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





