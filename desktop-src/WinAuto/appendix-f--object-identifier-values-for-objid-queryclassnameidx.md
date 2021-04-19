---
title: OBJID_QUERYCLASSNAMEIDX 的附錄 F 物件識別碼值
description: 當 OLEACC 傳送 \_ lParam 參數設定為 OBJIDQUERYCLASSNAMEIDX 的 WM GETOBJECT 訊息時，許多標準使用者或通用控制項 (COMCTL) 會傳回下列其中一個值。
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966467"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="191fd-103">附錄 F： OBJID QUERYCLASSNAMEIDX 的物件識別碼值 \_</span><span class="sxs-lookup"><span data-stu-id="191fd-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="191fd-104">當 OLEACC 傳送 *lParam* 參數設定為 OBJIDQUERYCLASSNAMEIDX 的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息時，許多標準使用者或通用控制項 (COMCTL) 會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="191fd-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="191fd-105">使用者或通用控制項</span><span class="sxs-lookup"><span data-stu-id="191fd-105">USER or common control</span></span> | <span data-ttu-id="191fd-106">傳回值</span><span class="sxs-lookup"><span data-stu-id="191fd-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="191fd-107">Listbox</span><span class="sxs-lookup"><span data-stu-id="191fd-107">Listbox</span></span>                | <span data-ttu-id="191fd-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="191fd-108">65536+0</span></span>      |
| <span data-ttu-id="191fd-109">按鈕</span><span class="sxs-lookup"><span data-stu-id="191fd-109">Button</span></span>                 | <span data-ttu-id="191fd-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="191fd-110">65536+2</span></span>      |
| <span data-ttu-id="191fd-111">Static</span><span class="sxs-lookup"><span data-stu-id="191fd-111">Static</span></span>                 | <span data-ttu-id="191fd-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="191fd-112">65536+3</span></span>      |
| <span data-ttu-id="191fd-113">編輯</span><span class="sxs-lookup"><span data-stu-id="191fd-113">Edit</span></span>                   | <span data-ttu-id="191fd-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="191fd-114">65536+4</span></span>      |
| <span data-ttu-id="191fd-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="191fd-115">Combobox</span></span>               | <span data-ttu-id="191fd-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="191fd-116">65536+5</span></span>      |
| <span data-ttu-id="191fd-117">捲軸</span><span class="sxs-lookup"><span data-stu-id="191fd-117">Scrollbar</span></span>              | <span data-ttu-id="191fd-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="191fd-118">65536+10</span></span>     |
| <span data-ttu-id="191fd-119">狀態</span><span class="sxs-lookup"><span data-stu-id="191fd-119">Status</span></span>                 | <span data-ttu-id="191fd-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="191fd-120">65536+11</span></span>     |
| <span data-ttu-id="191fd-121">工具列</span><span class="sxs-lookup"><span data-stu-id="191fd-121">Toolbar</span></span>                | <span data-ttu-id="191fd-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="191fd-122">65536+12</span></span>     |
| <span data-ttu-id="191fd-123">進度</span><span class="sxs-lookup"><span data-stu-id="191fd-123">Progress</span></span>               | <span data-ttu-id="191fd-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="191fd-124">65536+13</span></span>     |
| <span data-ttu-id="191fd-125">動畫</span><span class="sxs-lookup"><span data-stu-id="191fd-125">Animate</span></span>                | <span data-ttu-id="191fd-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="191fd-126">65536+14</span></span>     |
| <span data-ttu-id="191fd-127">索引標籤</span><span class="sxs-lookup"><span data-stu-id="191fd-127">Tab</span></span>                    | <span data-ttu-id="191fd-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="191fd-128">65536+15</span></span>     |
| <span data-ttu-id="191fd-129">熱鍵</span><span class="sxs-lookup"><span data-stu-id="191fd-129">Hotkey</span></span>                 | <span data-ttu-id="191fd-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="191fd-130">65536+16</span></span>     |
| <span data-ttu-id="191fd-131">標頭</span><span class="sxs-lookup"><span data-stu-id="191fd-131">Header</span></span>                 | <span data-ttu-id="191fd-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="191fd-132">65536+17</span></span>     |
| <span data-ttu-id="191fd-133">跟蹤</span><span class="sxs-lookup"><span data-stu-id="191fd-133">Trackbar</span></span>               | <span data-ttu-id="191fd-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="191fd-134">65536+18</span></span>     |
| <span data-ttu-id="191fd-135">Listview</span><span class="sxs-lookup"><span data-stu-id="191fd-135">Listview</span></span>               | <span data-ttu-id="191fd-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="191fd-136">65536+19</span></span>     |
| <span data-ttu-id="191fd-137">上下按鈕</span><span class="sxs-lookup"><span data-stu-id="191fd-137">Updown</span></span>                 | <span data-ttu-id="191fd-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="191fd-138">65536+22</span></span>     |
| <span data-ttu-id="191fd-139">提示</span><span class="sxs-lookup"><span data-stu-id="191fd-139">ToolTips</span></span>               | <span data-ttu-id="191fd-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="191fd-140">65536+24</span></span>     |
| <span data-ttu-id="191fd-141">Treeview</span><span class="sxs-lookup"><span data-stu-id="191fd-141">Treeview</span></span>               | <span data-ttu-id="191fd-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="191fd-142">65536+25</span></span>     |
| <span data-ttu-id="191fd-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="191fd-143">RichEdit</span></span>               | <span data-ttu-id="191fd-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="191fd-144">65536+28</span></span>     |



 

<span data-ttu-id="191fd-145">只有使用者和 Windows 通用控制項 (COMCTL) 會傳回資料表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="191fd-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="191fd-146">如果視窗傳回0以回應此訊息，則視窗可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="191fd-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="191fd-147">自訂控制項</span><span class="sxs-lookup"><span data-stu-id="191fd-147">A custom control</span></span>
-   <span data-ttu-id="191fd-148">上表中一個控制項以外的控制項</span><span class="sxs-lookup"><span data-stu-id="191fd-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="191fd-149">無法辨識 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息的舊版系統控制項</span><span class="sxs-lookup"><span data-stu-id="191fd-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="191fd-150">如果視窗傳回0，用戶端可能需要使用 [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) 或 [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)。</span><span class="sxs-lookup"><span data-stu-id="191fd-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="191fd-151">您可以使用這些函式來判斷以類別名稱為基礎的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="191fd-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="191fd-152">一般而言，用戶端可以使用 OLEACC 所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="191fd-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 