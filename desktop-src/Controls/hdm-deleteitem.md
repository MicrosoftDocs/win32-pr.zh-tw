---
title: 'HDM_DELETEITEM 訊息 (Commctrl .h) '
description: 從標題控制項刪除專案。 您可以明確地傳送此訊息，或使用標頭 \_ DeleteItem 宏。
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025253"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="ec65d-105">HDM \_ DELETEITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="ec65d-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="ec65d-106">從標題控制項刪除專案。</span><span class="sxs-lookup"><span data-stu-id="ec65d-106">Deletes an item from a header control.</span></span> <span data-ttu-id="ec65d-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="ec65d-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec65d-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec65d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec65d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec65d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec65d-110">要刪除之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="ec65d-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="ec65d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec65d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ec65d-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ec65d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec65d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec65d-113">Return value</span></span>

<span data-ttu-id="ec65d-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ec65d-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec65d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec65d-115">Requirements</span></span>



| <span data-ttu-id="ec65d-116">需求</span><span class="sxs-lookup"><span data-stu-id="ec65d-116">Requirement</span></span> | <span data-ttu-id="ec65d-117">值</span><span class="sxs-lookup"><span data-stu-id="ec65d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec65d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec65d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec65d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec65d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec65d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec65d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec65d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec65d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec65d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ec65d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec65d-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec65d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





