---
description: 適當地命名視窗和設定 Tablet PC 的視窗標題。
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: 適當地命名視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988329"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="1a584-103">適當地命名視窗</span><span class="sxs-lookup"><span data-stu-id="1a584-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="1a584-104">將使用者易記的標題指派給每個視窗，即使視窗或其標題為不可見。</span><span class="sxs-lookup"><span data-stu-id="1a584-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="1a584-105">這可讓語音功能識別視窗和視窗階層。</span><span class="sxs-lookup"><span data-stu-id="1a584-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="1a584-106">此建議適用于所有視窗：具有可見畫面格的最上層視窗;子視窗，例如浮動調色板;自訂控制項;工具列以及視窗內的窗格（實作為子視窗時）。</span><span class="sxs-lookup"><span data-stu-id="1a584-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="1a584-107">有三種方式可以設定視窗標題：</span><span class="sxs-lookup"><span data-stu-id="1a584-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="1a584-108">呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或相關函式時，請在資源腳本中設定字串。</span><span class="sxs-lookup"><span data-stu-id="1a584-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="1a584-109">呼叫 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="1a584-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="1a584-110">使用在 [對話方塊中命名控制項](naming-controls-in-dialog-boxes.md)中所述的技術，在對話方塊中定義控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a584-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="1a584-111">這是標記編輯控制項的唯一方法，因為設定控制項內建標籤會變更控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="1a584-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="1a584-112">您可以使用 Microsoft Active Accessibility 或 WM GETTEXT 訊息來查詢標題 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1a584-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="1a584-113">如需使用 Active Accessibility 來查詢標題的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility) 一節。</span><span class="sxs-lookup"><span data-stu-id="1a584-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
