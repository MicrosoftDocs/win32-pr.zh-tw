---
title: 'LVM_GETTOPINDEX 訊息 (Commctrl .h) '
description: 在清單或報表檢視中，抓取最上層可見專案的索引。 您可以明確地傳送此訊息，或使用 ListView \_ GetTopIndex 宏來傳送。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967753"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="5d48e-105">LVM \_ GETTOPINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="5d48e-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="5d48e-106">在清單或報表檢視中，抓取最上層可見專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5d48e-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="5d48e-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="5d48e-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d48e-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d48e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d48e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d48e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d48e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d48e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d48e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d48e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d48e-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5d48e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d48e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d48e-113">Return value</span></span>

<span data-ttu-id="5d48e-114">如果成功，則傳回專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5d48e-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="5d48e-115">如果清單視圖控制項在圖示或小型圖示視圖中，或如果清單視圖控制項在已啟用群組的詳細資料檢視中，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="5d48e-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d48e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d48e-116">Requirements</span></span>



| <span data-ttu-id="5d48e-117">需求</span><span class="sxs-lookup"><span data-stu-id="5d48e-117">Requirement</span></span> | <span data-ttu-id="5d48e-118">值</span><span class="sxs-lookup"><span data-stu-id="5d48e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d48e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d48e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5d48e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d48e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d48e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d48e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5d48e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d48e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d48e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5d48e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d48e-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d48e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





