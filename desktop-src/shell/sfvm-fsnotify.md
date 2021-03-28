---
description: 通知回呼物件，該事件發生了會影響其中一個專案的事件。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_FSNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2021
ms.locfileid: "104991834"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="5f83c-104">SFVM \_ FSNOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="5f83c-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="5f83c-105">通知回呼物件，該事件發生了會影響其中一個專案的事件。</span><span class="sxs-lookup"><span data-stu-id="5f83c-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="5f83c-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="5f83c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="5f83c-107">參數</span><span class="sxs-lookup"><span data-stu-id="5f83c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f83c-108">*ppidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f83c-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f83c-109">受影響專案之 PIDL 的指標。</span><span class="sxs-lookup"><span data-stu-id="5f83c-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="5f83c-110">*lEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f83c-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f83c-111">指出發生之事件的 SHCNE 值。</span><span class="sxs-lookup"><span data-stu-id="5f83c-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="5f83c-112">如需可能值的清單，請參閱 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)。</span><span class="sxs-lookup"><span data-stu-id="5f83c-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f83c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f83c-113">Requirements</span></span>



| <span data-ttu-id="5f83c-114">需求</span><span class="sxs-lookup"><span data-stu-id="5f83c-114">Requirement</span></span> | <span data-ttu-id="5f83c-115">值</span><span class="sxs-lookup"><span data-stu-id="5f83c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f83c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f83c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f83c-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f83c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5f83c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f83c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f83c-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f83c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5f83c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5f83c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f83c-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f83c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
