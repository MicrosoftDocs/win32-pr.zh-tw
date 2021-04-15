---
description: 註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 此訊息可 \_ 讓您指定特定的監視，以擴充 ABM SETAUTOHIDEBAR，以便在多個監視器的情況下使用。
title: 'ABM_SETAUTOHIDEBAREX 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992455"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="dab8d-104">ABM \_ SETAUTOHIDEBAREX 訊息</span><span class="sxs-lookup"><span data-stu-id="dab8d-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="dab8d-105">註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="dab8d-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="dab8d-106">此訊息可讓您指定特定的監視，以擴充 [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) ，以便在多個監視器的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="dab8d-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="dab8d-107">參數</span><span class="sxs-lookup"><span data-stu-id="dab8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab8d-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="dab8d-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="dab8d-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dab8d-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="dab8d-110">將 **lParam** 成員設為 **TRUE** 以註冊 appbar 或 **FALSE** 將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="dab8d-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="dab8d-111">傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge**、 **rc** 和 **lParam** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="dab8d-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab8d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dab8d-112">Return value</span></span>

<span data-ttu-id="dab8d-113">如果成功，則傳回 **TRUE** ; 如果發生錯誤，或如果已在指定的監視器上為指定的邊緣註冊自動隱藏 appbar，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="dab8d-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab8d-114">備註</span><span class="sxs-lookup"><span data-stu-id="dab8d-114">Remarks</span></span>

<span data-ttu-id="dab8d-115">系統只允許每個監視器的每個邊緣都有一個自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="dab8d-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="dab8d-116">此監視器取決於 **rc** 成員，而邊緣是由 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的 **uEdge** 成員所決定。</span><span class="sxs-lookup"><span data-stu-id="dab8d-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab8d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dab8d-117">Requirements</span></span>



| <span data-ttu-id="dab8d-118">需求</span><span class="sxs-lookup"><span data-stu-id="dab8d-118">Requirement</span></span> | <span data-ttu-id="dab8d-119">值</span><span class="sxs-lookup"><span data-stu-id="dab8d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dab8d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dab8d-120">Header</span></span><br/> | <dl> <span data-ttu-id="dab8d-121"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dab8d-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab8d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dab8d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab8d-123">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="dab8d-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="dab8d-124">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="dab8d-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="dab8d-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="dab8d-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




