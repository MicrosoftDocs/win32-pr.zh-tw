---
description: 抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 此訊息可 \_ 讓您指定特定的監視，以擴充 ABM GETAUTOHIDEBAR，以便在多個監視器的情況下使用。
title: 'ABM_GETAUTOHIDEBAREX 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974857"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="94b0f-104">ABM \_ GETAUTOHIDEBAREX 訊息</span><span class="sxs-lookup"><span data-stu-id="94b0f-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="94b0f-105">抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。</span><span class="sxs-lookup"><span data-stu-id="94b0f-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="94b0f-106">此訊息可讓您指定特定的監視，以擴充 [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) ，以便在多個監視器的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="94b0f-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="94b0f-107">參數</span><span class="sxs-lookup"><span data-stu-id="94b0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b0f-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="94b0f-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="94b0f-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，指定螢幕邊緣和監視器。</span><span class="sxs-lookup"><span data-stu-id="94b0f-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="94b0f-110">傳送此訊息時，您必須指定 **cbSize**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="94b0f-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94b0f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="94b0f-111">Return value</span></span>

<span data-ttu-id="94b0f-112">將控制碼傳回到自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="94b0f-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="94b0f-113">如果發生錯誤，或沒有自動隱藏 appbar 與指定監視器的指定邊緣相關聯，則傳回值為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="94b0f-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="94b0f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="94b0f-114">Requirements</span></span>



| <span data-ttu-id="94b0f-115">需求</span><span class="sxs-lookup"><span data-stu-id="94b0f-115">Requirement</span></span> | <span data-ttu-id="94b0f-116">值</span><span class="sxs-lookup"><span data-stu-id="94b0f-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94b0f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="94b0f-117">Header</span></span><br/> | <dl> <span data-ttu-id="94b0f-118"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="94b0f-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b0f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94b0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b0f-120">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="94b0f-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="94b0f-121">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="94b0f-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="94b0f-122">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="94b0f-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




