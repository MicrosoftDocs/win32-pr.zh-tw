---
description: 註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 如果系統有多個監視器，則會使用包含主要工作列的監視器。
title: 'ABM_SETAUTOHIDEBAR 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972097"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="7c963-104">ABM \_ SETAUTOHIDEBAR 訊息</span><span class="sxs-lookup"><span data-stu-id="7c963-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="7c963-105">註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="7c963-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="7c963-106">如果系統有多個監視器，則會使用包含主要工作列的監視器。</span><span class="sxs-lookup"><span data-stu-id="7c963-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="7c963-107">若要在特定監視器上註冊或取消註冊自動隱藏 appbar，請使用 [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)。</span><span class="sxs-lookup"><span data-stu-id="7c963-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="7c963-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c963-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c963-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="7c963-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="7c963-110">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7c963-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="7c963-111">將 **lParam** 成員設定為 **TRUE** ，即可註冊 appbar 或 **FALSE** 以將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="7c963-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="7c963-112">傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **lParam** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7c963-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c963-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c963-113">Return value</span></span>

<span data-ttu-id="7c963-114">如果成功，則傳回 **TRUE** ; 如果發生錯誤，或如果已為指定的邊緣註冊自動隱藏 appbar，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7c963-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c963-115">備註</span><span class="sxs-lookup"><span data-stu-id="7c963-115">Remarks</span></span>

<span data-ttu-id="7c963-116">系統只允許畫面的每個邊緣都有一個自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="7c963-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="7c963-117">當設定 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的成員 **uEdge** 時，就會決定這一點。</span><span class="sxs-lookup"><span data-stu-id="7c963-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c963-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c963-118">Requirements</span></span>



| <span data-ttu-id="7c963-119">需求</span><span class="sxs-lookup"><span data-stu-id="7c963-119">Requirement</span></span> | <span data-ttu-id="7c963-120">值</span><span class="sxs-lookup"><span data-stu-id="7c963-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c963-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c963-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c963-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c963-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c963-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c963-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c963-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c963-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c963-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7c963-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c963-126"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c963-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c963-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c963-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c963-128">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="7c963-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="7c963-129">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="7c963-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="7c963-130">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="7c963-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




