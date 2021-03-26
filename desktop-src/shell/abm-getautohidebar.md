---
description: 抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 如果系統有多個監視器，則會使用包含主要工作列的監視器。
title: 'ABM_GETAUTOHIDEBAR 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112364"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="8b808-104">ABM \_ GETAUTOHIDEBAR 訊息</span><span class="sxs-lookup"><span data-stu-id="8b808-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="8b808-105">抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b808-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="8b808-106">如果系統有多個監視器，則會使用包含主要工作列的監視器。</span><span class="sxs-lookup"><span data-stu-id="8b808-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="8b808-107">若要查詢特定監視器上的自動隱藏 appbar，請使用 [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)。</span><span class="sxs-lookup"><span data-stu-id="8b808-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="8b808-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b808-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b808-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="8b808-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="8b808-110">指定螢幕邊緣之 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8b808-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="8b808-111">傳送此訊息時，您必須指定 **cbSize** 和 **uEdge** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="8b808-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b808-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b808-112">Return value</span></span>

<span data-ttu-id="8b808-113">將控制碼傳回到自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="8b808-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="8b808-114">如果發生錯誤，或如果沒有自動隱藏 appbar 與指定的邊緣相關聯，則傳回值為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8b808-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b808-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b808-115">Requirements</span></span>



| <span data-ttu-id="8b808-116">需求</span><span class="sxs-lookup"><span data-stu-id="8b808-116">Requirement</span></span> | <span data-ttu-id="8b808-117">值</span><span class="sxs-lookup"><span data-stu-id="8b808-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b808-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b808-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b808-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b808-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8b808-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b808-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b808-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b808-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b808-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8b808-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b808-123"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b808-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b808-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b808-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b808-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="8b808-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="8b808-126">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="8b808-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="8b808-127">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="8b808-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




