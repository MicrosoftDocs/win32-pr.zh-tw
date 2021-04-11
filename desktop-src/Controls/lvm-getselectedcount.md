---
title: 'LVM_GETSELECTEDCOUNT 訊息 (Commctrl .h) '
description: 決定清單視圖控制項中選取的專案數目。 您可以明確地傳送此訊息，或使用 ListView \_ GetSelectedCount 宏來傳送。
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844092"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="2f607-105">LVM \_ GETSELECTEDCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="2f607-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="2f607-106">決定清單視圖控制項中選取的專案數目。</span><span class="sxs-lookup"><span data-stu-id="2f607-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="2f607-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="2f607-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f607-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f607-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f607-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f607-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f607-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2f607-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f607-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f607-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f607-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2f607-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f607-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f607-113">Return value</span></span>

<span data-ttu-id="2f607-114">傳回選取之專案的數目。</span><span class="sxs-lookup"><span data-stu-id="2f607-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f607-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f607-115">Requirements</span></span>



| <span data-ttu-id="2f607-116">需求</span><span class="sxs-lookup"><span data-stu-id="2f607-116">Requirement</span></span> | <span data-ttu-id="2f607-117">值</span><span class="sxs-lookup"><span data-stu-id="2f607-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f607-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f607-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f607-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f607-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f607-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f607-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f607-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f607-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f607-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2f607-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f607-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f607-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





