---
title: 'LVN_ODCACHEHINT (Commctrl 的通知碼) '
description: 由虛擬清單-view 控制項在其顯示區域的內容變更時傳送。
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935166"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="20da4-104">LVN \_ ODCACHEHINT 通知碼</span><span class="sxs-lookup"><span data-stu-id="20da4-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="20da4-105">由虛擬清單-view 控制項在其顯示區域的內容變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="20da4-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="20da4-106">例如，當使用者滾動控制項的顯示時，清單視圖控制項會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="20da4-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="20da4-107">LVN \_ ODCACHEHINT 通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="20da4-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="20da4-108">參數</span><span class="sxs-lookup"><span data-stu-id="20da4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20da4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20da4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20da4-110">[**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)結構的指標，其中包含要快取之專案範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="20da4-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20da4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="20da4-111">Return value</span></span>

<span data-ttu-id="20da4-112">接收此通知碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="20da4-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="20da4-113">備註</span><span class="sxs-lookup"><span data-stu-id="20da4-113">Remarks</span></span>

<span data-ttu-id="20da4-114">處理此訊息可讓應用程式更新保留在快取中的專案資訊，以便在傳送 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知碼時立即可供使用。</span><span class="sxs-lookup"><span data-stu-id="20da4-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="20da4-115">請注意，此通知碼不一定是 [LVN \_ GETDISPINFO](lvn-getdispinfo.md)所要求之專案的確切表示。</span><span class="sxs-lookup"><span data-stu-id="20da4-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="20da4-116">因此，如果在處理 LVN GETDISPINFO 時未快取要求的專案 \_ ，應用程式必須準備好從快取外部的來源提供要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="20da4-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="20da4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="20da4-117">Requirements</span></span>



| <span data-ttu-id="20da4-118">需求</span><span class="sxs-lookup"><span data-stu-id="20da4-118">Requirement</span></span> | <span data-ttu-id="20da4-119">值</span><span class="sxs-lookup"><span data-stu-id="20da4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20da4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20da4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20da4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20da4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20da4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20da4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20da4-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20da4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20da4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="20da4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="20da4-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="20da4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





