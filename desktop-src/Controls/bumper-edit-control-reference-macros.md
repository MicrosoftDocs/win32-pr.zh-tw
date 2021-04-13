---
title: 編輯控制項宏
description: 編輯控制項宏
ms.assetid: 7c2bb80e-57ca-4d95-a499-b65eefe0352c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795aba77e2f0dc439fdd6bdaab6a4358a15596ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322143"
---
# <a name="edit-control-macros"></a><span data-ttu-id="c05d3-103">編輯控制項宏</span><span class="sxs-lookup"><span data-stu-id="c05d3-103">Edit Control Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c05d3-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="c05d3-104">In this section</span></span>

-   [<span data-ttu-id="c05d3-105">**編輯 \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="c05d3-105">**Edit\_CanUndo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_canundo)
-   [<span data-ttu-id="c05d3-106">**編輯 \_ EmptyUndoBuffer**</span><span class="sxs-lookup"><span data-stu-id="c05d3-106">**Edit\_EmptyUndoBuffer**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_emptyundobuffer)
-   [<span data-ttu-id="c05d3-107">**編輯 \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="c05d3-107">**Edit\_Enable**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_enable)
-   [<span data-ttu-id="c05d3-108">**編輯 \_ FmtLines**</span><span class="sxs-lookup"><span data-stu-id="c05d3-108">**Edit\_FmtLines**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_fmtlines)
-   [<span data-ttu-id="c05d3-109">**編輯 \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="c05d3-109">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
-   [<span data-ttu-id="c05d3-110">**編輯 \_ GetFirstVisibleLine**</span><span class="sxs-lookup"><span data-stu-id="c05d3-110">**Edit\_GetFirstVisibleLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getfirstvisibleline)
-   [<span data-ttu-id="c05d3-111">**編輯 \_ GetHandle**</span><span class="sxs-lookup"><span data-stu-id="c05d3-111">**Edit\_GetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gethandle)
-   [<span data-ttu-id="c05d3-112">**編輯 \_ GetHilite**</span><span class="sxs-lookup"><span data-stu-id="c05d3-112">**Edit\_GetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_gethilite)
-   [<span data-ttu-id="c05d3-113">**編輯 \_ GetLine**</span><span class="sxs-lookup"><span data-stu-id="c05d3-113">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
-   [<span data-ttu-id="c05d3-114">**編輯 \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="c05d3-114">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
-   [<span data-ttu-id="c05d3-115">**編輯 \_ GetModify**</span><span class="sxs-lookup"><span data-stu-id="c05d3-115">**Edit\_GetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getmodify)
-   [<span data-ttu-id="c05d3-116">**編輯 \_ GetPasswordChar**</span><span class="sxs-lookup"><span data-stu-id="c05d3-116">**Edit\_GetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getpasswordchar)
-   [<span data-ttu-id="c05d3-117">**編輯 \_ GetRect**</span><span class="sxs-lookup"><span data-stu-id="c05d3-117">**Edit\_GetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getrect)
-   [<span data-ttu-id="c05d3-118">**編輯 \_ GetSel**</span><span class="sxs-lookup"><span data-stu-id="c05d3-118">**Edit\_GetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getsel)
-   [<span data-ttu-id="c05d3-119">**編輯 \_ GetText**</span><span class="sxs-lookup"><span data-stu-id="c05d3-119">**Edit\_GetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettext)
-   [<span data-ttu-id="c05d3-120">**編輯 \_ GetTextLength**</span><span class="sxs-lookup"><span data-stu-id="c05d3-120">**Edit\_GetTextLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettextlength)
-   [<span data-ttu-id="c05d3-121">**編輯 \_ GetWordBreakProc**</span><span class="sxs-lookup"><span data-stu-id="c05d3-121">**Edit\_GetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getwordbreakproc)
-   [<span data-ttu-id="c05d3-122">**編輯 \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="c05d3-122">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
-   [<span data-ttu-id="c05d3-123">**編輯 \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="c05d3-123">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
-   [<span data-ttu-id="c05d3-124">**編輯 \_ LineFromChar**</span><span class="sxs-lookup"><span data-stu-id="c05d3-124">**Edit\_LineFromChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linefromchar)
-   [<span data-ttu-id="c05d3-125">**編輯 \_ LineIndex**</span><span class="sxs-lookup"><span data-stu-id="c05d3-125">**Edit\_LineIndex**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_lineindex)
-   [<span data-ttu-id="c05d3-126">**編輯 \_ LineLength**</span><span class="sxs-lookup"><span data-stu-id="c05d3-126">**Edit\_LineLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linelength)
-   [<span data-ttu-id="c05d3-127">**編輯 \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="c05d3-127">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
-   [<span data-ttu-id="c05d3-128">**編輯 \_ ReplaceSel**</span><span class="sxs-lookup"><span data-stu-id="c05d3-128">**Edit\_ReplaceSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_replacesel)
-   [<span data-ttu-id="c05d3-129">**編輯 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="c05d3-129">**Edit\_Scroll**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scroll)
-   [<span data-ttu-id="c05d3-130">**編輯 \_ ScrollCaret**</span><span class="sxs-lookup"><span data-stu-id="c05d3-130">**Edit\_ScrollCaret**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scrollcaret)
-   [<span data-ttu-id="c05d3-131">**編輯 \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="c05d3-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
-   [<span data-ttu-id="c05d3-132">**編輯 \_ SetCueBannerTextFocused**</span><span class="sxs-lookup"><span data-stu-id="c05d3-132">**Edit\_SetCueBannerTextFocused**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertextfocused)
-   [<span data-ttu-id="c05d3-133">**編輯 \_ SetHandle**</span><span class="sxs-lookup"><span data-stu-id="c05d3-133">**Edit\_SetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_sethandle)
-   [<span data-ttu-id="c05d3-134">**編輯 \_ SetHilite**</span><span class="sxs-lookup"><span data-stu-id="c05d3-134">**Edit\_SetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_sethilite)
-   [<span data-ttu-id="c05d3-135">**編輯 \_ SetModify**</span><span class="sxs-lookup"><span data-stu-id="c05d3-135">**Edit\_SetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setmodify)
-   [<span data-ttu-id="c05d3-136">**編輯 \_ SetPasswordChar**</span><span class="sxs-lookup"><span data-stu-id="c05d3-136">**Edit\_SetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setpasswordchar)
-   [<span data-ttu-id="c05d3-137">**編輯 \_ SetReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c05d3-137">**Edit\_SetReadOnly**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setreadonly)
-   [<span data-ttu-id="c05d3-138">**編輯 \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="c05d3-138">**Edit\_SetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrect)
-   [<span data-ttu-id="c05d3-139">**編輯 \_ SetRectNoPaint**</span><span class="sxs-lookup"><span data-stu-id="c05d3-139">**Edit\_SetRectNoPaint**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrectnopaint)
-   [<span data-ttu-id="c05d3-140">**編輯 \_ SetSel**</span><span class="sxs-lookup"><span data-stu-id="c05d3-140">**Edit\_SetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setsel)
-   [<span data-ttu-id="c05d3-141">**編輯 \_ SetTabStops**</span><span class="sxs-lookup"><span data-stu-id="c05d3-141">**Edit\_SetTabStops**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settabstops)
-   [<span data-ttu-id="c05d3-142">**編輯 \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="c05d3-142">**Edit\_SetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settext)
-   [<span data-ttu-id="c05d3-143">**編輯 \_ SetWordBreakProc**</span><span class="sxs-lookup"><span data-stu-id="c05d3-143">**Edit\_SetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setwordbreakproc)
-   [<span data-ttu-id="c05d3-144">**編輯 \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="c05d3-144">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
-   [<span data-ttu-id="c05d3-145">**編輯 \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="c05d3-145">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
-   [<span data-ttu-id="c05d3-146">**編輯 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="c05d3-146">**Edit\_Undo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_undo)

 

 




