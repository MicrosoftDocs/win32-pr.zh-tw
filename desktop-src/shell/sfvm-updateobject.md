---
description: 藉由將指標指向 (Pidl) 的專案識別碼清單，將指標傳遞至兩個指標的陣列，以更新物件。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_UPDATEOBJECT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195325"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="b1521-104">SFVM \_ UPDATEOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="b1521-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="b1521-105">藉由將指標指向 (Pidl) 的專案識別碼清單，將指標傳遞至兩個指標的陣列，以更新物件。</span><span class="sxs-lookup"><span data-stu-id="b1521-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="b1521-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="b1521-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="b1521-107">參數</span><span class="sxs-lookup"><span data-stu-id="b1521-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1521-108">*ppidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1521-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1521-109">兩個 Pidl 陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="b1521-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="b1521-110">第一個 PIDL 是舊的 PIDL。</span><span class="sxs-lookup"><span data-stu-id="b1521-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="b1521-111">第二個是舊 PIDL 的複本，其中包含更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="b1521-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="b1521-112">成功完成此呼叫後，對複製的存留期的控制權會屬於 view。</span><span class="sxs-lookup"><span data-stu-id="b1521-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1521-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1521-113">Return value</span></span>

<span data-ttu-id="b1521-114">如果更新成功，則傳回已更新物件的 listview 識別碼;否則，它會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="b1521-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1521-115">備註</span><span class="sxs-lookup"><span data-stu-id="b1521-115">Remarks</span></span>

<span data-ttu-id="b1521-116">如果更新失敗，則呼叫端必須釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="b1521-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1521-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1521-117">Requirements</span></span>



| <span data-ttu-id="b1521-118">需求</span><span class="sxs-lookup"><span data-stu-id="b1521-118">Requirement</span></span> | <span data-ttu-id="b1521-119">值</span><span class="sxs-lookup"><span data-stu-id="b1521-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1521-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1521-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b1521-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1521-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b1521-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1521-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b1521-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1521-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b1521-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b1521-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1521-125"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1521-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




