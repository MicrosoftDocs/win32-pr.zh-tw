---
title: 'TCM_DELETEITEM 訊息 (Commctrl .h) '
description: 從索引標籤控制項移除專案。 您可以使用 TabCtrl DeleteItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934950"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="717db-105">TCM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="717db-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="717db-106">從索引標籤控制項移除專案。</span><span class="sxs-lookup"><span data-stu-id="717db-106">Removes an item from a tab control.</span></span> <span data-ttu-id="717db-107">您可以使用 [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="717db-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="717db-108">參數</span><span class="sxs-lookup"><span data-stu-id="717db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="717db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="717db-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="717db-110">要刪除之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="717db-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="717db-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="717db-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="717db-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="717db-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="717db-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="717db-113">Return value</span></span>

<span data-ttu-id="717db-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="717db-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="717db-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="717db-115">Requirements</span></span>



| <span data-ttu-id="717db-116">需求</span><span class="sxs-lookup"><span data-stu-id="717db-116">Requirement</span></span> | <span data-ttu-id="717db-117">值</span><span class="sxs-lookup"><span data-stu-id="717db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="717db-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="717db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="717db-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="717db-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="717db-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="717db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="717db-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="717db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="717db-122">標頭</span><span class="sxs-lookup"><span data-stu-id="717db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="717db-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="717db-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





