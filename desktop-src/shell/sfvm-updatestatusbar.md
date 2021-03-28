---
description: 通知回呼物件正在更新狀態列。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_UPDATESTATUSBAR 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991630"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="35735-104">SFVM \_ UPDATESTATUSBAR 訊息</span><span class="sxs-lookup"><span data-stu-id="35735-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="35735-105">通知回呼物件正在更新狀態列。</span><span class="sxs-lookup"><span data-stu-id="35735-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="35735-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="35735-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="35735-107">參數</span><span class="sxs-lookup"><span data-stu-id="35735-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35735-108">*fInitialize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35735-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35735-109">如果正在初始化狀態列，則 **布林** 值會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="35735-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35735-110">備註</span><span class="sxs-lookup"><span data-stu-id="35735-110">Remarks</span></span>

<span data-ttu-id="35735-111">當您收到此通知時：</span><span class="sxs-lookup"><span data-stu-id="35735-111">When you receive this notification:</span></span>

-   <span data-ttu-id="35735-112">\_如果您將會處理更新，請返回 S。</span><span class="sxs-lookup"><span data-stu-id="35735-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="35735-113">Return \_ 會讓 HRESULT (嚴重性 \_ 成功，0，1) ，讓系統資料夾 view 物件設定狀態列文字。</span><span class="sxs-lookup"><span data-stu-id="35735-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="35735-114">Return E \_ 無法讓系統資料夾 view 物件處理狀態列。</span><span class="sxs-lookup"><span data-stu-id="35735-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="35735-115">預設狀態列文字如下所示。</span><span class="sxs-lookup"><span data-stu-id="35735-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="35735-116">狀態</span><span class="sxs-lookup"><span data-stu-id="35735-116">Status</span></span>                      | <span data-ttu-id="35735-117">狀態列文字</span><span class="sxs-lookup"><span data-stu-id="35735-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="35735-118">未選取任何專案</span><span class="sxs-lookup"><span data-stu-id="35735-118">No items selected</span></span>           | <span data-ttu-id="35735-119">\# \# 資料夾中的 "objects" () </span><span class="sxs-lookup"><span data-stu-id="35735-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="35735-120">已選取一個專案</span><span class="sxs-lookup"><span data-stu-id="35735-120">One item selected</span></span>           | <span data-ttu-id="35735-121">專案的提示（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="35735-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="35735-122">選取了一個以上的專案</span><span class="sxs-lookup"><span data-stu-id="35735-122">More than one item selected</span></span> | <span data-ttu-id="35735-123">「 \# \# 選取的物件」</span><span class="sxs-lookup"><span data-stu-id="35735-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="35735-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="35735-124">Requirements</span></span>



| <span data-ttu-id="35735-125">需求</span><span class="sxs-lookup"><span data-stu-id="35735-125">Requirement</span></span> | <span data-ttu-id="35735-126">值</span><span class="sxs-lookup"><span data-stu-id="35735-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35735-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35735-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35735-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35735-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="35735-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35735-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35735-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35735-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="35735-131">標頭</span><span class="sxs-lookup"><span data-stu-id="35735-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35735-132"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="35735-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
