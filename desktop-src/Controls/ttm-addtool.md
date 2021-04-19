---
title: 'TTM_ADDTOOL 訊息 (Commctrl .h) '
description: 使用工具提示控制項註冊工具。
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999815"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="bb751-104">TTM \_ ADDTOOL 訊息</span><span class="sxs-lookup"><span data-stu-id="bb751-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="bb751-105">使用工具提示控制項註冊工具。</span><span class="sxs-lookup"><span data-stu-id="bb751-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb751-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb751-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb751-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb751-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bb751-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb751-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb751-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb751-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，其中包含工具提示控制項顯示工具文字所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="bb751-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="bb751-111">傳送此訊息之前，必須先填入此結構的 **cbSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="bb751-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb751-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb751-112">Return value</span></span>

<span data-ttu-id="bb751-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bb751-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb751-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb751-114">Requirements</span></span>



| <span data-ttu-id="bb751-115">需求</span><span class="sxs-lookup"><span data-stu-id="bb751-115">Requirement</span></span> | <span data-ttu-id="bb751-116">值</span><span class="sxs-lookup"><span data-stu-id="bb751-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb751-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb751-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb751-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb751-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb751-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb751-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb751-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb751-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb751-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bb751-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb751-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb751-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bb751-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="bb751-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb751-124">**TTM \_ADDTOOLW** (Unicode) 和 **TTM \_ ADDTOOLA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="bb751-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="bb751-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb751-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb751-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="bb751-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb751-127">**TTM \_ DELTOOL**</span><span class="sxs-lookup"><span data-stu-id="bb751-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="bb751-128">**概念**</span><span class="sxs-lookup"><span data-stu-id="bb751-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb751-129">關於工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="bb751-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





