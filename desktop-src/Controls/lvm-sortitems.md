---
title: 'LVM_SORTITEMS 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 ListView \_ SortItems 宏來傳送。
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935173"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="482d2-106">LVM \_ SORTITEMS 訊息</span><span class="sxs-lookup"><span data-stu-id="482d2-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="482d2-107">使用應用程式定義的比較函式來排序清單視圖控制項的專案。</span><span class="sxs-lookup"><span data-stu-id="482d2-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="482d2-108">每個專案的索引都會變更，以反映新的序列。</span><span class="sxs-lookup"><span data-stu-id="482d2-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="482d2-109">您可以明確地傳送此訊息，或使用 [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="482d2-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="482d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="482d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482d2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="482d2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="482d2-112">傳遞給比較函數的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="482d2-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="482d2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="482d2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="482d2-114">應用程式定義的比較函式的指標。</span><span class="sxs-lookup"><span data-stu-id="482d2-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="482d2-115">每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫比較函數。</span><span class="sxs-lookup"><span data-stu-id="482d2-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482d2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="482d2-116">Return value</span></span>

<span data-ttu-id="482d2-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="482d2-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="482d2-118">備註</span><span class="sxs-lookup"><span data-stu-id="482d2-118">Remarks</span></span>

<span data-ttu-id="482d2-119">比較函數的形式如下：</span><span class="sxs-lookup"><span data-stu-id="482d2-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="482d2-120">*LParam1* 參數是與第一個要比較的專案相關聯的值，而 *lParam2* 參數則是與第二個專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="482d2-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="482d2-121">這些值是在專案插入清單中時，在專案的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **lParam** 成員中指定的值。</span><span class="sxs-lookup"><span data-stu-id="482d2-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="482d2-122">[**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)的 *wParam* 參數會傳遞給回呼函式，做為它的第三個參數。</span><span class="sxs-lookup"><span data-stu-id="482d2-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="482d2-123">如果第一個專案應該在第二個專案之前，比較函式必須傳回負值，如果第一個專案應接在第二個專案，則為正值，如果兩個專案相等，則為零。</span><span class="sxs-lookup"><span data-stu-id="482d2-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="482d2-124">在排序過程中，清單視圖內容不穩定。</span><span class="sxs-lookup"><span data-stu-id="482d2-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="482d2-125">如果回呼函式將任何訊息傳送至 GETITEM 的 LVM GETITEM 以外的 [**LVM \_**](lvm-getitem.md) 控制項， ([**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) ，結果就是無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="482d2-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="482d2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="482d2-126">Requirements</span></span>



| <span data-ttu-id="482d2-127">需求</span><span class="sxs-lookup"><span data-stu-id="482d2-127">Requirement</span></span> | <span data-ttu-id="482d2-128">值</span><span class="sxs-lookup"><span data-stu-id="482d2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="482d2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="482d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="482d2-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="482d2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="482d2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="482d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="482d2-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="482d2-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="482d2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="482d2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="482d2-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="482d2-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





