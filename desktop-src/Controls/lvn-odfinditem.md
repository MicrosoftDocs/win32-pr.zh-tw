---
title: 'LVN_ODFINDITEM 訊息 (Commctrl .h) '
description: 當需要擁有者尋找特定回呼專案時，由虛擬清單-view 控制項傳送。
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104813"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="07c48-104">LVN \_ ODFINDITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="07c48-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="07c48-105">當需要擁有者尋找特定回呼專案時，由 [虛擬清單-view](list-view-controls-overview.md) 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="07c48-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="07c48-106">例如，當此控制項收到快速鍵鍵盤輸入或收到 [**LVM \_ FINDITEM**](lvm-finditem.md) 訊息時，會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="07c48-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="07c48-107">LVN \_ ODFINDITEM 通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="07c48-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="07c48-108">參數</span><span class="sxs-lookup"><span data-stu-id="07c48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07c48-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07c48-110">[**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)結構的指標，其中包含要用於搜尋的資訊。</span><span class="sxs-lookup"><span data-stu-id="07c48-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c48-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="07c48-111">Return value</span></span>

<span data-ttu-id="07c48-112">傳回找到之專案的索引，如果找不到任何專案，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="07c48-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c48-113">備註</span><span class="sxs-lookup"><span data-stu-id="07c48-113">Remarks</span></span>

<span data-ttu-id="07c48-114">搜尋資訊會以 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) 結構的形式傳送，這是 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="07c48-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c48-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="07c48-115">Requirements</span></span>



| <span data-ttu-id="07c48-116">需求</span><span class="sxs-lookup"><span data-stu-id="07c48-116">Requirement</span></span> | <span data-ttu-id="07c48-117">值</span><span class="sxs-lookup"><span data-stu-id="07c48-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07c48-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07c48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07c48-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07c48-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07c48-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07c48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07c48-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07c48-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07c48-122">標頭</span><span class="sxs-lookup"><span data-stu-id="07c48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c48-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="07c48-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="07c48-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="07c48-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="07c48-125">**LVN \_ODFINDITEMW** (Unicode) 和 **LVN \_ ODFINDITEMA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="07c48-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





