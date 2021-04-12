---
title: 'HDM_INSERTITEM 訊息 (Commctrl .h) '
description: 將新的專案插入至標題控制項。 您可以明確地傳送此訊息，或使用標頭 \_ InsertItem 宏。
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465376"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="b06ab-105">HDM \_ INSERTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="b06ab-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="b06ab-106">將新的專案插入至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="b06ab-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="b06ab-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) 宏。</span><span class="sxs-lookup"><span data-stu-id="b06ab-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b06ab-108">參數</span><span class="sxs-lookup"><span data-stu-id="b06ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b06ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b06ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b06ab-110">要插入新專案的專案索引。</span><span class="sxs-lookup"><span data-stu-id="b06ab-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="b06ab-111">如果 *wParam* 大於或等於控制項中的專案數，則新專案會插入至標題控制項的結尾。</span><span class="sxs-lookup"><span data-stu-id="b06ab-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="b06ab-112">如果 *wParam* 為零，則會在標題控制項的開頭插入新專案。</span><span class="sxs-lookup"><span data-stu-id="b06ab-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="b06ab-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b06ab-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b06ab-114">[**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的指標，其中包含新專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b06ab-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b06ab-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b06ab-115">Return value</span></span>

<span data-ttu-id="b06ab-116">如果成功，則傳回新專案的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="b06ab-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b06ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b06ab-117">Requirements</span></span>



| <span data-ttu-id="b06ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="b06ab-118">Requirement</span></span> | <span data-ttu-id="b06ab-119">值</span><span class="sxs-lookup"><span data-stu-id="b06ab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b06ab-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b06ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b06ab-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b06ab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b06ab-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b06ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b06ab-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b06ab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b06ab-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b06ab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b06ab-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b06ab-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b06ab-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b06ab-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b06ab-127">**HDM \_INSERTITEMW** (Unicode) 和 **HDM \_ INSERTITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b06ab-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





