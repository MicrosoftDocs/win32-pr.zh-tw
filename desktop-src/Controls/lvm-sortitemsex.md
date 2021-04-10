---
title: 'LVM_SORTITEMSEX 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 ListView \_ SortItemsEx 宏來傳送。
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024663"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="0827f-106">LVM \_ SORTITEMSEX 訊息</span><span class="sxs-lookup"><span data-stu-id="0827f-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="0827f-107">使用應用程式定義的比較函式來排序清單視圖控制項的專案。</span><span class="sxs-lookup"><span data-stu-id="0827f-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="0827f-108">每個專案的索引都會變更，以反映新的序列。</span><span class="sxs-lookup"><span data-stu-id="0827f-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="0827f-109">您可以明確地傳送此訊息，或使用 [**ListView \_ SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="0827f-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0827f-110">參數</span><span class="sxs-lookup"><span data-stu-id="0827f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0827f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0827f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0827f-112">傳遞給比較函數的應用程式定義值。</span><span class="sxs-lookup"><span data-stu-id="0827f-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="0827f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0827f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0827f-114">應用程式定義的比較函式的指標。</span><span class="sxs-lookup"><span data-stu-id="0827f-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="0827f-115">每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫它。</span><span class="sxs-lookup"><span data-stu-id="0827f-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0827f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0827f-116">Return value</span></span>

<span data-ttu-id="0827f-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0827f-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0827f-118">備註</span><span class="sxs-lookup"><span data-stu-id="0827f-118">Remarks</span></span>

<span data-ttu-id="0827f-119">比較函數的形式如下：</span><span class="sxs-lookup"><span data-stu-id="0827f-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="0827f-120">此訊息類似于 [**LVM \_ SORTITEMS**](lvm-sortitems.md)，但傳遞給比較函數的資訊類型除外。</span><span class="sxs-lookup"><span data-stu-id="0827f-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="0827f-121">使用 **LVM \_ SORTITEMSEX**， *lParam1* 是第一個專案的目前索引，而 *lParam2* 是第二個專案的目前索引。</span><span class="sxs-lookup"><span data-stu-id="0827f-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="0827f-122">如有需要，您可以傳送 [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) 訊息來取得專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0827f-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="0827f-123">如果第一個專案應該在第二個專案之前，比較函式必須傳回負值，如果第一個專案應接在第二個專案，則為正值，如果兩個專案相等，則為零。</span><span class="sxs-lookup"><span data-stu-id="0827f-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="0827f-124">在排序過程中，清單視圖內容不穩定。</span><span class="sxs-lookup"><span data-stu-id="0827f-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="0827f-125">如果回呼函式將任何訊息傳送至 GETITEM 的 LVM GETITEM 以外的 [**LVM \_**](lvm-getitem.md) 控制項， ([**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) ，結果就是無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="0827f-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0827f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0827f-126">Requirements</span></span>



| <span data-ttu-id="0827f-127">需求</span><span class="sxs-lookup"><span data-stu-id="0827f-127">Requirement</span></span> | <span data-ttu-id="0827f-128">值</span><span class="sxs-lookup"><span data-stu-id="0827f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0827f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0827f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0827f-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0827f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0827f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0827f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0827f-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0827f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0827f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="0827f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0827f-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0827f-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





