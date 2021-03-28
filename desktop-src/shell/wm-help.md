---
description: 指出使用者按下 F1 鍵。
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: 'WM_HELP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973104"
---
# <a name="wm_help-message"></a><span data-ttu-id="ca1bb-103">WM 說明 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="ca1bb-103">WM\_HELP message</span></span>

<span data-ttu-id="ca1bb-104">指出使用者按下 F1 鍵。</span><span class="sxs-lookup"><span data-stu-id="ca1bb-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="ca1bb-105">如果按下 F1 時，功能表為使用中狀態，則會將 **wm \_** 說明傳送至與功能表相關聯的視窗; 否則，會將 wm 說明傳送至具有鍵盤焦點的視窗。 **\_**</span><span class="sxs-lookup"><span data-stu-id="ca1bb-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="ca1bb-106">如果沒有任何視窗具有鍵盤焦點， **則 \_ 會將 WM** 說明傳送至目前的使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="ca1bb-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca1bb-107">參數</span><span class="sxs-lookup"><span data-stu-id="ca1bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca1bb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca1bb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca1bb-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ca1bb-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca1bb-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="ca1bb-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="ca1bb-111">[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的位址，其中包含已要求說明之功能表項目、控制項、對話方塊或視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca1bb-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca1bb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca1bb-112">Return value</span></span>

<span data-ttu-id="ca1bb-113">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ca1bb-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca1bb-114">備註</span><span class="sxs-lookup"><span data-stu-id="ca1bb-114">Remarks</span></span>

<span data-ttu-id="ca1bb-115">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將 WM 說明傳遞給子視窗的父視窗，或傳遞至最上層視窗的擁有者。 **\_**</span><span class="sxs-lookup"><span data-stu-id="ca1bb-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca1bb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca1bb-116">Requirements</span></span>



| <span data-ttu-id="ca1bb-117">需求</span><span class="sxs-lookup"><span data-stu-id="ca1bb-117">Requirement</span></span> | <span data-ttu-id="ca1bb-118">值</span><span class="sxs-lookup"><span data-stu-id="ca1bb-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1bb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca1bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1bb-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca1bb-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ca1bb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca1bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1bb-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca1bb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ca1bb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ca1bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca1bb-124"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca1bb-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
