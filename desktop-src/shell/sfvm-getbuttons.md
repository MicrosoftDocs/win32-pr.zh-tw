---
description: 允許回呼物件指定要加入至工具列的按鈕。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: 'SFVM_GETBUTTONS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850664"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="24d7c-104">SFVM \_ GETBUTTONS 訊息</span><span class="sxs-lookup"><span data-stu-id="24d7c-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="24d7c-105">允許回呼物件指定要加入至工具列的按鈕。</span><span class="sxs-lookup"><span data-stu-id="24d7c-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="24d7c-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="24d7c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="24d7c-107">參數</span><span class="sxs-lookup"><span data-stu-id="24d7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d7c-108">中的 *idCmdFirst \_ cbtnMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="24d7c-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24d7c-109">包含使用 [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) 宏封裝到參數中的 2 16 位值。</span><span class="sxs-lookup"><span data-stu-id="24d7c-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="24d7c-110">低序位字組包含初始命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="24d7c-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="24d7c-111">高序位單字包含要加入的按鈕數目（如先前的 [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) 訊息中所指定）。</span><span class="sxs-lookup"><span data-stu-id="24d7c-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="24d7c-112">*pbtn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24d7c-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24d7c-113">[**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton)結構陣列的位址，每個要新增至工具列的按鈕各有一個位址。</span><span class="sxs-lookup"><span data-stu-id="24d7c-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24d7c-114">備註</span><span class="sxs-lookup"><span data-stu-id="24d7c-114">Remarks</span></span>

<span data-ttu-id="24d7c-115">此訊息的前面會有 [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="24d7c-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="24d7c-116">回呼物件必須處理該訊息，以指定按鈕的數目，以及要在工具列上放置它們的位置。</span><span class="sxs-lookup"><span data-stu-id="24d7c-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="24d7c-117">根據回呼物件回應 **SFVM \_ GETBUTTONINFO** 訊息的方式， *pbtn* 參數所指定的按鈕將會附加到系統資料夾 view 物件的標準按鈕或前面，或是取代標準集。</span><span class="sxs-lookup"><span data-stu-id="24d7c-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d7c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="24d7c-118">Requirements</span></span>



| <span data-ttu-id="24d7c-119">需求</span><span class="sxs-lookup"><span data-stu-id="24d7c-119">Requirement</span></span> | <span data-ttu-id="24d7c-120">值</span><span class="sxs-lookup"><span data-stu-id="24d7c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="24d7c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24d7c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24d7c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24d7c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="24d7c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24d7c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24d7c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24d7c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="24d7c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="24d7c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24d7c-126"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="24d7c-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
