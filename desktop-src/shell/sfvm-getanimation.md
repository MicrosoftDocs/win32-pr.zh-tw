---
description: 允許回呼物件指定在背景執行緒上列舉專案時顯示動畫。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: 'SFVM_GETANIMATION 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115833"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="a72c2-104">SFVM \_ GETANIMATION 訊息</span><span class="sxs-lookup"><span data-stu-id="a72c2-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="a72c2-105">允許回呼物件指定在背景執行緒上列舉專案時顯示動畫。</span><span class="sxs-lookup"><span data-stu-id="a72c2-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="a72c2-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="a72c2-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="a72c2-107">參數</span><span class="sxs-lookup"><span data-stu-id="a72c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a72c2-108">*phinst* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a72c2-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a72c2-109">應從中載入資源之模組的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="a72c2-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="a72c2-110">*pwszName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a72c2-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a72c2-111">以 null 終止的 Unicode 字串指標，其中包含 .avi 檔案的路徑或 AVI 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a72c2-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="a72c2-112">或者，此參數可以包含低序位字組中的資源識別碼，以及高序位字組中的0。</span><span class="sxs-lookup"><span data-stu-id="a72c2-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="a72c2-113">若要建立這個值，請使用 [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) 宏。</span><span class="sxs-lookup"><span data-stu-id="a72c2-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="a72c2-114">控制項會從 hinst 所指定的模組載入資源。</span><span class="sxs-lookup"><span data-stu-id="a72c2-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="a72c2-115">AVI 資源必須有 "AVI" 類型。</span><span class="sxs-lookup"><span data-stu-id="a72c2-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a72c2-116">備註</span><span class="sxs-lookup"><span data-stu-id="a72c2-116">Remarks</span></span>

<span data-ttu-id="a72c2-117">根據預設，系統資料夾 view 物件會在背景列舉期間顯示「底圖」動畫。</span><span class="sxs-lookup"><span data-stu-id="a72c2-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="a72c2-118">*phinst* 和 *pwszName* 將會傳遞至具有「已 [**\_ 開啟**](../controls/acm-open.md)」訊息的 [動畫控制項](../controls/animation-control-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a72c2-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a72c2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a72c2-119">Requirements</span></span>



| <span data-ttu-id="a72c2-120">需求</span><span class="sxs-lookup"><span data-stu-id="a72c2-120">Requirement</span></span> | <span data-ttu-id="a72c2-121">值</span><span class="sxs-lookup"><span data-stu-id="a72c2-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a72c2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a72c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a72c2-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72c2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a72c2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a72c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a72c2-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72c2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a72c2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a72c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a72c2-127"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="a72c2-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
