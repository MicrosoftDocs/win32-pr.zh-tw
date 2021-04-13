---
title: 'TCM_DELETEALLITEMS 訊息 (Commctrl .h) '
description: 從索引標籤控制項移除所有專案。 您可以使用 TabCtrl DeleteAllItems 宏明確地傳送此訊息 \_ 。
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509215"
---
# <a name="tcm_deleteallitems-message"></a><span data-ttu-id="69cee-105">TCM \_ DELETEALLITEMS 訊息</span><span class="sxs-lookup"><span data-stu-id="69cee-105">TCM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="69cee-106">從索引標籤控制項移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="69cee-106">Removes all items from a tab control.</span></span> <span data-ttu-id="69cee-107">您可以使用 [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="69cee-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="69cee-108">參數</span><span class="sxs-lookup"><span data-stu-id="69cee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69cee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69cee-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="69cee-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="69cee-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="69cee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69cee-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="69cee-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="69cee-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69cee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="69cee-113">Return value</span></span>

<span data-ttu-id="69cee-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="69cee-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cee-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="69cee-115">Requirements</span></span>



| <span data-ttu-id="69cee-116">需求</span><span class="sxs-lookup"><span data-stu-id="69cee-116">Requirement</span></span> | <span data-ttu-id="69cee-117">值</span><span class="sxs-lookup"><span data-stu-id="69cee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69cee-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69cee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69cee-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69cee-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69cee-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69cee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69cee-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69cee-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69cee-122">標頭</span><span class="sxs-lookup"><span data-stu-id="69cee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="69cee-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="69cee-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





