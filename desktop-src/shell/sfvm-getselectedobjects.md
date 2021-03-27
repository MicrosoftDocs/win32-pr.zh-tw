---
description: 針對所有選取的物件，抓取專案識別碼清單的指標陣列 (Pidl) 。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_GETSELECTEDOBJECTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852580"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="4a1e7-104">SFVM \_ GETSELECTEDOBJECTS 訊息</span><span class="sxs-lookup"><span data-stu-id="4a1e7-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="4a1e7-105">針對所有選取的物件，抓取專案識別碼清單的指標陣列 (Pidl) 。</span><span class="sxs-lookup"><span data-stu-id="4a1e7-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="4a1e7-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="4a1e7-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="4a1e7-107">參數</span><span class="sxs-lookup"><span data-stu-id="4a1e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1e7-108">*ppidl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a1e7-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="4a1e7-109">目前所選物件之 Pidl 陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="4a1e7-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1e7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a1e7-110">Return value</span></span>

<span data-ttu-id="4a1e7-111">傳回陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="4a1e7-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a1e7-112">備註</span><span class="sxs-lookup"><span data-stu-id="4a1e7-112">Remarks</span></span>

<span data-ttu-id="4a1e7-113">完成時，您應該在陣列的每個成員上呼叫 [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) ，以釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a1e7-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1e7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a1e7-114">Requirements</span></span>



| <span data-ttu-id="4a1e7-115">需求</span><span class="sxs-lookup"><span data-stu-id="4a1e7-115">Requirement</span></span> | <span data-ttu-id="4a1e7-116">值</span><span class="sxs-lookup"><span data-stu-id="4a1e7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1e7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a1e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1e7-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a1e7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4a1e7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a1e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1e7-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a1e7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a1e7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4a1e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a1e7-122"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a1e7-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




