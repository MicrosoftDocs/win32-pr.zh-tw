---
description: 允許回呼物件在顯示 Windows 檔案總管快顯功能表之前加以修改。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_INITMENUPOPUP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973789"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="761f3-104">SFVM \_ INITMENUPOPUP 訊息</span><span class="sxs-lookup"><span data-stu-id="761f3-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="761f3-105">允許回呼物件在顯示 Windows 檔案總管快顯功能表之前加以修改。</span><span class="sxs-lookup"><span data-stu-id="761f3-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="761f3-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="761f3-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="761f3-107">參數</span><span class="sxs-lookup"><span data-stu-id="761f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="761f3-108">中的 *idCmd \_ nIndex* \[\]</span><span class="sxs-lookup"><span data-stu-id="761f3-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761f3-109">此參數的低序位字組會保留為用戶端命令保留的第一個命令識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="761f3-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="761f3-110">高序位單字會保存功能表的索引。</span><span class="sxs-lookup"><span data-stu-id="761f3-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="761f3-111">*hmenu* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="761f3-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="761f3-112">功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="761f3-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="761f3-113">備註</span><span class="sxs-lookup"><span data-stu-id="761f3-113">Remarks</span></span>

<span data-ttu-id="761f3-114">當您選取功能表時，但在顯示之前，系統資料夾 view 物件會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="761f3-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="761f3-115">舉例來說，如果您需要啟用或停用功能表命令，請處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="761f3-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="761f3-116">快顯功能表可以是：</span><span class="sxs-lookup"><span data-stu-id="761f3-116">The popup menu can be:</span></span>

-   <span data-ttu-id="761f3-117">[檔案]、[編輯] 或 [流覽] 功能表。</span><span class="sxs-lookup"><span data-stu-id="761f3-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="761f3-118">用戶端所定義的最上層功能表。</span><span class="sxs-lookup"><span data-stu-id="761f3-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="761f3-119">用戶端定義的子功能表。</span><span class="sxs-lookup"><span data-stu-id="761f3-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="761f3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="761f3-120">Requirements</span></span>



| <span data-ttu-id="761f3-121">需求</span><span class="sxs-lookup"><span data-stu-id="761f3-121">Requirement</span></span> | <span data-ttu-id="761f3-122">值</span><span class="sxs-lookup"><span data-stu-id="761f3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="761f3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="761f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="761f3-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="761f3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="761f3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="761f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="761f3-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="761f3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="761f3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="761f3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="761f3-128"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="761f3-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="761f3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="761f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761f3-130">**SFVM \_ MERGEMENU**</span><span class="sxs-lookup"><span data-stu-id="761f3-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
