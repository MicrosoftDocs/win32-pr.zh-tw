---
description: SFVM \_ THISIDLIST 可能已變更或無法使用。
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: 'SFVM_THISIDLIST 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695439"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="f22b6-103">SFVM \_ THISIDLIST 訊息</span><span class="sxs-lookup"><span data-stu-id="f22b6-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="f22b6-104">\[**SFVM \_THISIDLIST** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f22b6-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f22b6-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f22b6-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f22b6-106">允許回呼物件指定 (PIDL) 之專案識別碼清單的視圖指標。</span><span class="sxs-lookup"><span data-stu-id="f22b6-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="f22b6-107">只有當 [**IPersistIDList：： SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) 和 [**IPersistFolder2：： GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) 失敗時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="f22b6-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="f22b6-108">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="f22b6-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="f22b6-109">參數</span><span class="sxs-lookup"><span data-stu-id="f22b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f22b6-110">*pidl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f22b6-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f22b6-111">視圖 PIDL 的位址。</span><span class="sxs-lookup"><span data-stu-id="f22b6-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f22b6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22b6-112">Requirements</span></span>



| <span data-ttu-id="f22b6-113">需求</span><span class="sxs-lookup"><span data-stu-id="f22b6-113">Requirement</span></span> | <span data-ttu-id="f22b6-114">值</span><span class="sxs-lookup"><span data-stu-id="f22b6-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f22b6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f22b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f22b6-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22b6-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f22b6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f22b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f22b6-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22b6-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f22b6-119">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f22b6-119">End of client support</span></span><br/>    | <span data-ttu-id="f22b6-120">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="f22b6-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="f22b6-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f22b6-121">End of server support</span></span><br/>    | <span data-ttu-id="f22b6-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f22b6-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="f22b6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f22b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f22b6-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="f22b6-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
