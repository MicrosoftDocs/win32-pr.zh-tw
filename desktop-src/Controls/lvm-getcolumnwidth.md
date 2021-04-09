---
title: 'LVM_GETCOLUMNWIDTH 訊息 (Commctrl .h) '
description: 取得報表或清單視圖中資料行的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumnWidth 宏來傳送。
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093848"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="6d47b-105">LVM \_ GETCOLUMNWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="6d47b-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="6d47b-106">取得報表或清單視圖中資料行的寬度。</span><span class="sxs-lookup"><span data-stu-id="6d47b-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="6d47b-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6d47b-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d47b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d47b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d47b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d47b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d47b-110">資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="6d47b-110">The index of the column.</span></span> <span data-ttu-id="6d47b-111">清單視圖中會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="6d47b-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="6d47b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d47b-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6d47b-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6d47b-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d47b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d47b-114">Return value</span></span>

<span data-ttu-id="6d47b-115">如果成功，則傳回資料行寬度，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="6d47b-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="6d47b-116">如果此訊息傳送至具有 [**lvs) \_ 報表**](list-view-window-styles.md) 樣式的清單視圖控制項，而且指定的資料行不存在，則傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="6d47b-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d47b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d47b-117">Requirements</span></span>



| <span data-ttu-id="6d47b-118">需求</span><span class="sxs-lookup"><span data-stu-id="6d47b-118">Requirement</span></span> | <span data-ttu-id="6d47b-119">值</span><span class="sxs-lookup"><span data-stu-id="6d47b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d47b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d47b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6d47b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d47b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d47b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d47b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6d47b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d47b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d47b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6d47b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d47b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d47b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





