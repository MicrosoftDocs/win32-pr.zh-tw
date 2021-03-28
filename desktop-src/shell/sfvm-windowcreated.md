---
description: 通知回呼物件正在建立資料夾檢視視窗。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_WINDOWCREATED 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973805"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="8c378-104">SFVM \_ WINDOWCREATED 訊息</span><span class="sxs-lookup"><span data-stu-id="8c378-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="8c378-105">通知回呼物件正在建立資料夾檢視視窗。</span><span class="sxs-lookup"><span data-stu-id="8c378-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="8c378-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="8c378-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="8c378-107">參數</span><span class="sxs-lookup"><span data-stu-id="8c378-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c378-108">*hwndView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c378-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c378-109">資料夾檢視的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c378-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c378-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c378-110">Requirements</span></span>



| <span data-ttu-id="8c378-111">需求</span><span class="sxs-lookup"><span data-stu-id="8c378-111">Requirement</span></span> | <span data-ttu-id="8c378-112">值</span><span class="sxs-lookup"><span data-stu-id="8c378-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c378-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c378-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8c378-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c378-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c378-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c378-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8c378-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c378-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c378-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8c378-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c378-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c378-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
