---
title: 'LVM_GETEXTENDEDLISTVIEWSTYLE 訊息 (Commctrl .h) '
description: 取得目前用於指定清單視圖控制項的延伸樣式。 您可以明確地傳送此訊息，或使用 ListView \_ GetExtendedListViewStyle 宏。
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024591"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="5429d-105">LVM \_ GETEXTENDEDLISTVIEWSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="5429d-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="5429d-106">取得目前用於指定清單視圖控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="5429d-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="5429d-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="5429d-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5429d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5429d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5429d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5429d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5429d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5429d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5429d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5429d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5429d-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5429d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5429d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5429d-113">Return value</span></span>

<span data-ttu-id="5429d-114">傳回 **DWORD** ，表示指定清單視圖控制項目前使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="5429d-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="5429d-115">這個值可以是 [延伸 List-View 樣式](extended-list-view-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="5429d-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5429d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5429d-116">Requirements</span></span>



| <span data-ttu-id="5429d-117">需求</span><span class="sxs-lookup"><span data-stu-id="5429d-117">Requirement</span></span> | <span data-ttu-id="5429d-118">值</span><span class="sxs-lookup"><span data-stu-id="5429d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5429d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5429d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5429d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5429d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5429d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5429d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5429d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5429d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5429d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5429d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5429d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5429d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





