---
description: 通知容器網站的回呼物件。 只有當不支援 IObjectWithSite：： SetSite 且使用 SHCreateShellFolderViewEx 時，才會使用這個。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: 'SFVM_SETISFV 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973812"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="88ea0-105">SFVM \_ SETISFV 訊息</span><span class="sxs-lookup"><span data-stu-id="88ea0-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="88ea0-106">\[這項通知是透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 支援。</span><span class="sxs-lookup"><span data-stu-id="88ea0-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="88ea0-107">後續版本的 Windows 可能不支援此功能。\]</span><span class="sxs-lookup"><span data-stu-id="88ea0-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="88ea0-108">通知容器網站的回呼物件。</span><span class="sxs-lookup"><span data-stu-id="88ea0-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="88ea0-109">只有當不支援 [**IObjectWithSite：： SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) 且使用 [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) 時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="88ea0-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="88ea0-110">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="88ea0-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="88ea0-111">參數</span><span class="sxs-lookup"><span data-stu-id="88ea0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ea0-112">*網站* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88ea0-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ea0-113">容器網站的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="88ea0-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88ea0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="88ea0-114">Requirements</span></span>



| <span data-ttu-id="88ea0-115">需求</span><span class="sxs-lookup"><span data-stu-id="88ea0-115">Requirement</span></span> | <span data-ttu-id="88ea0-116">值</span><span class="sxs-lookup"><span data-stu-id="88ea0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88ea0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88ea0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="88ea0-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88ea0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88ea0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88ea0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="88ea0-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88ea0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88ea0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="88ea0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="88ea0-122"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="88ea0-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
