---
description: 當使用者在已將本身註冊為已卸載檔案收件者的應用程式視窗上放置檔案時傳送。
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: 'WM_DROPFILES 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973105"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="4af98-103">WM \_ DROPFILES 訊息</span><span class="sxs-lookup"><span data-stu-id="4af98-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="4af98-104">當使用者在已將本身註冊為已卸載檔案收件者的應用程式視窗上放置檔案時傳送。</span><span class="sxs-lookup"><span data-stu-id="4af98-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="4af98-105">參數</span><span class="sxs-lookup"><span data-stu-id="4af98-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4af98-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="4af98-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="4af98-107">描述已卸載檔案之內部結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4af98-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="4af98-108">將此控制碼傳遞給 [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish)、 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)或 [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) ，以取得已卸載檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4af98-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="4af98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4af98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4af98-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4af98-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4af98-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4af98-111">Return value</span></span>

<span data-ttu-id="4af98-112">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="4af98-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af98-113">備註</span><span class="sxs-lookup"><span data-stu-id="4af98-113">Remarks</span></span>

<span data-ttu-id="4af98-114">HDROP 控制碼是在 Shellapi 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="4af98-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="4af98-115">您必須在組建中包含此標頭，才能使用 **WM \_ DROPFILES**。</span><span class="sxs-lookup"><span data-stu-id="4af98-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="4af98-116">如需如何使用拖放來傳送 Shell 資料的進一步討論，請參閱 [使用拖放或剪貼簿來傳送 Shell 資料](dragdrop.md)。</span><span class="sxs-lookup"><span data-stu-id="4af98-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4af98-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4af98-117">Requirements</span></span>



| <span data-ttu-id="4af98-118">需求</span><span class="sxs-lookup"><span data-stu-id="4af98-118">Requirement</span></span> | <span data-ttu-id="4af98-119">值</span><span class="sxs-lookup"><span data-stu-id="4af98-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4af98-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4af98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4af98-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4af98-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4af98-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4af98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4af98-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4af98-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4af98-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4af98-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4af98-125"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="4af98-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4af98-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4af98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af98-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="4af98-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="4af98-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="4af98-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
