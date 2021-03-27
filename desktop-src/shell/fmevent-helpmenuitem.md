---
description: 當使用者按下功能表或工具列命令專案上的 F1 時，傳送至檔案管理員延伸模組 DLL 程式。 擴充功能應該呼叫 WinHelp，並將該函式的 hwnd 參數設定為延伸模組的 hwnd 參數值。
title: 'FMEVENT_HELPMENUITEM 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971917"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="05a9e-104">FMEVENT \_ HELPMENUITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="05a9e-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="05a9e-105">當使用者按下功能表或工具列命令專案上的 F1 時，傳送至檔案管理員延伸模組 DLL 程式。</span><span class="sxs-lookup"><span data-stu-id="05a9e-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="05a9e-106">擴充功能應該呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)，並將該函式的 *hwnd* 參數設定為延伸模組的 *hwnd* 參數值。</span><span class="sxs-lookup"><span data-stu-id="05a9e-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="05a9e-107">參數</span><span class="sxs-lookup"><span data-stu-id="05a9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a9e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05a9e-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="05a9e-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="05a9e-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="05a9e-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="05a9e-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="05a9e-111">識別所需說明之功能表或工具列命令專案的值。</span><span class="sxs-lookup"><span data-stu-id="05a9e-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="05a9e-112">擴充程式會使用這個值來判斷呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="05a9e-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a9e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="05a9e-113">Return value</span></span>

<span data-ttu-id="05a9e-114">如果延伸 DLL 程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="05a9e-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a9e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a9e-115">Requirements</span></span>



| <span data-ttu-id="05a9e-116">需求</span><span class="sxs-lookup"><span data-stu-id="05a9e-116">Requirement</span></span> | <span data-ttu-id="05a9e-117">值</span><span class="sxs-lookup"><span data-stu-id="05a9e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05a9e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05a9e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="05a9e-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a9e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="05a9e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05a9e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="05a9e-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a9e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05a9e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="05a9e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a9e-123"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="05a9e-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a9e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a9e-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="05a9e-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="05a9e-126">**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="05a9e-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




