---
title: 'LVM_DELETECOLUMN 訊息 (Commctrl .h) '
description: 從清單視圖控制項移除資料行。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteColumn 宏來傳送。
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685525"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="766f9-105">LVM \_ DELETECOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="766f9-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="766f9-106">從清單視圖控制項移除資料行。</span><span class="sxs-lookup"><span data-stu-id="766f9-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="766f9-107">您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="766f9-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="766f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="766f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="766f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="766f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="766f9-110">要刪除之資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="766f9-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="766f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="766f9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="766f9-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="766f9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="766f9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="766f9-113">Return value</span></span>

<span data-ttu-id="766f9-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="766f9-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="766f9-115">備註</span><span class="sxs-lookup"><span data-stu-id="766f9-115">Remarks</span></span>

<span data-ttu-id="766f9-116">只有 ComCtl32.dll 6 版和更新版本才支援刪除清單視圖控制項中的資料行零。</span><span class="sxs-lookup"><span data-stu-id="766f9-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="766f9-117">第5版也支援刪除資料行零，但只有在您使用 [**CCM \_ SETVERSION**](ccm-setversion.md) 將版本設定為5或更新版本之後。</span><span class="sxs-lookup"><span data-stu-id="766f9-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="766f9-118">在第5版之前的版本中，如果您必須刪除資料行零，請插入零長度的虛擬資料行零，並刪除一或多個資料行。</span><span class="sxs-lookup"><span data-stu-id="766f9-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="766f9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="766f9-119">Requirements</span></span>



| <span data-ttu-id="766f9-120">需求</span><span class="sxs-lookup"><span data-stu-id="766f9-120">Requirement</span></span> | <span data-ttu-id="766f9-121">值</span><span class="sxs-lookup"><span data-stu-id="766f9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="766f9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="766f9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="766f9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="766f9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="766f9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="766f9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="766f9-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="766f9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="766f9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="766f9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="766f9-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="766f9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





