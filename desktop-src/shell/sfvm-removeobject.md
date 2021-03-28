---
description: 從 shell 視圖中移除物件。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_REMOVEOBJECT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973816"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="b1e8f-104">SFVM \_ REMOVEOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="b1e8f-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="b1e8f-105">從 shell 視圖中移除物件。</span><span class="sxs-lookup"><span data-stu-id="b1e8f-105">Removes an object from the shell view.</span></span> <span data-ttu-id="b1e8f-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="b1e8f-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="b1e8f-107">參數</span><span class="sxs-lookup"><span data-stu-id="b1e8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e8f-108">*pidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1e8f-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="b1e8f-109">要移除之物件的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="b1e8f-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e8f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1e8f-110">Return value</span></span>

<span data-ttu-id="b1e8f-111">如果找到符合指定之 PIDL 的專案，則傳回已移除之專案的索引;否則，會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="b1e8f-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e8f-112">備註</span><span class="sxs-lookup"><span data-stu-id="b1e8f-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e8f-113">需求</span><span class="sxs-lookup"><span data-stu-id="b1e8f-113">Requirements</span></span>



| <span data-ttu-id="b1e8f-114">需求</span><span class="sxs-lookup"><span data-stu-id="b1e8f-114">Requirement</span></span> | <span data-ttu-id="b1e8f-115">值</span><span class="sxs-lookup"><span data-stu-id="b1e8f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e8f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1e8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e8f-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1e8f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b1e8f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1e8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e8f-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1e8f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b1e8f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b1e8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e8f-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e8f-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




