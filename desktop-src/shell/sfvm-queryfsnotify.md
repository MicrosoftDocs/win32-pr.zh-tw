---
description: SFVM \_ QUERYFSNOTIFY 可能已變更或無法使用。
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: 'SFVM_QUERYFSNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195330"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="b46b6-103">SFVM \_ QUERYFSNOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="b46b6-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="b46b6-104">\[**SFVM \_QUERYFSNOTIFY** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b46b6-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b46b6-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b46b6-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b46b6-106">允許回呼物件註冊資料夾，讓該資料夾的視圖變更會產生通知。</span><span class="sxs-lookup"><span data-stu-id="b46b6-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="b46b6-107">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="b46b6-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="b46b6-108">參數</span><span class="sxs-lookup"><span data-stu-id="b46b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b46b6-109">*shcne* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b46b6-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b46b6-110">結構，用來保存要監看事件的專案 PIDL，以及指出是否也應該監看該專案的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="b46b6-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b46b6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b46b6-111">Requirements</span></span>



| <span data-ttu-id="b46b6-112">需求</span><span class="sxs-lookup"><span data-stu-id="b46b6-112">Requirement</span></span> | <span data-ttu-id="b46b6-113">值</span><span class="sxs-lookup"><span data-stu-id="b46b6-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b46b6-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b46b6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b46b6-115">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b46b6-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b46b6-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b46b6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b46b6-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b46b6-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b46b6-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b46b6-118">End of client support</span></span><br/>    | <span data-ttu-id="b46b6-119">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="b46b6-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="b46b6-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b46b6-120">End of server support</span></span><br/>    | <span data-ttu-id="b46b6-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b46b6-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="b46b6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b46b6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b46b6-123"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="b46b6-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
