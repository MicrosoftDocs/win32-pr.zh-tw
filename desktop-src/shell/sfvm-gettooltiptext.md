---
description: 允許回呼物件指定功能表項目或工具列按鈕的工具提示文字字串。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: 'SFVM_GETTOOLTIPTEXT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945263"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="2b622-104">SFVM \_ GETTOOLTIPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="2b622-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="2b622-105">允許回呼物件指定功能表項目或工具列按鈕的工具提示文字字串。</span><span class="sxs-lookup"><span data-stu-id="2b622-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="2b622-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="2b622-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="2b622-107">參數</span><span class="sxs-lookup"><span data-stu-id="2b622-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b622-108">中的 *idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="2b622-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b622-109">此參數的低序位字組會保存命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b622-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="2b622-110">高序位單字會保存 *pszText* 緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="2b622-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2b622-111">*pszText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b622-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b622-112">包含解說文字且以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="2b622-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b622-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b622-113">Requirements</span></span>



| <span data-ttu-id="2b622-114">需求</span><span class="sxs-lookup"><span data-stu-id="2b622-114">Requirement</span></span> | <span data-ttu-id="2b622-115">值</span><span class="sxs-lookup"><span data-stu-id="2b622-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b622-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b622-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b622-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b622-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b622-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b622-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b622-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b622-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2b622-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2b622-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b622-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b622-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
