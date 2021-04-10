---
title: 'HDM_ORDERTOINDEX 訊息 (Commctrl .h) '
description: 根據標題控制項中的順序，抓取專案的索引值。 您可以明確地傳送此訊息，或使用標頭 \_ OrderToIndex 宏。
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025032"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="19e24-105">HDM \_ ORDERTOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="19e24-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="19e24-106">根據標題控制項中的順序，抓取專案的索引值。</span><span class="sxs-lookup"><span data-stu-id="19e24-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="19e24-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) 宏。</span><span class="sxs-lookup"><span data-stu-id="19e24-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19e24-108">參數</span><span class="sxs-lookup"><span data-stu-id="19e24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19e24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19e24-110">專案在標題控制項內出現的順序，由左至右。</span><span class="sxs-lookup"><span data-stu-id="19e24-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="19e24-111">例如，在最左邊的資料行中，專案的索引值會是0。</span><span class="sxs-lookup"><span data-stu-id="19e24-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="19e24-112">右邊的下一個專案的值為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="19e24-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="19e24-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19e24-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="19e24-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="19e24-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e24-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="19e24-115">Return value</span></span>

<span data-ttu-id="19e24-116">傳回表示專案索引的 INT。</span><span class="sxs-lookup"><span data-stu-id="19e24-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="19e24-117">如果 *wParam* 無效 (負或太大) ，則傳回等於 *wParam*。</span><span class="sxs-lookup"><span data-stu-id="19e24-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e24-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e24-118">Requirements</span></span>



| <span data-ttu-id="19e24-119">需求</span><span class="sxs-lookup"><span data-stu-id="19e24-119">Requirement</span></span> | <span data-ttu-id="19e24-120">值</span><span class="sxs-lookup"><span data-stu-id="19e24-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19e24-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19e24-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19e24-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19e24-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19e24-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19e24-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19e24-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19e24-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19e24-125">標頭</span><span class="sxs-lookup"><span data-stu-id="19e24-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e24-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="19e24-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





