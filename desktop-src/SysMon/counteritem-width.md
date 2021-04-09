---
title: CounterItem Width 屬性
description: 抓取或設定用來繪製計數器值的線條寬度。
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- 寬度屬性 SysMon
- Width 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，Width 屬性
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685979"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="071e2-106">CounterItem Width 屬性</span><span class="sxs-lookup"><span data-stu-id="071e2-106">CounterItem.Width property</span></span>

<span data-ttu-id="071e2-107">抓取或設定用來繪製計數器值的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="071e2-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="071e2-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="071e2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="071e2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="071e2-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="071e2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="071e2-110">Property value</span></span>

<span data-ttu-id="071e2-111">線條圖形中所使用的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="071e2-111">Line width used in a line graph.</span></span> <span data-ttu-id="071e2-112">有效值的範圍從1到3，其中 1 (預設值) 是最小寬度。</span><span class="sxs-lookup"><span data-stu-id="071e2-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="071e2-113">**在 Windows Vista 之前：** 有效的值範圍從1到9。</span><span class="sxs-lookup"><span data-stu-id="071e2-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="071e2-114">如果您的應用程式將會在 Windows Vista 上執行，請勿使用大於3的寬度值。</span><span class="sxs-lookup"><span data-stu-id="071e2-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="071e2-115">例外狀況</span><span class="sxs-lookup"><span data-stu-id="071e2-115">Exceptions</span></span>



| <span data-ttu-id="071e2-116">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="071e2-116">Exception type</span></span>               | <span data-ttu-id="071e2-117">條件</span><span class="sxs-lookup"><span data-stu-id="071e2-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="071e2-118">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="071e2-118">**System.ArgumentException**</span></span> | <span data-ttu-id="071e2-119">指定的線條寬度無效。</span><span class="sxs-lookup"><span data-stu-id="071e2-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="071e2-120">備註</span><span class="sxs-lookup"><span data-stu-id="071e2-120">Remarks</span></span>

<span data-ttu-id="071e2-121">您新增的前十六個計數器的預設行寬度為1。</span><span class="sxs-lookup"><span data-stu-id="071e2-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="071e2-122">接下來16個計數器的預設行寬度 (您新增的計數器 17-32) ：2。</span><span class="sxs-lookup"><span data-stu-id="071e2-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="071e2-123">接下來16個計數器的預設行寬度 (計數器 33-48) 您新增的是3。</span><span class="sxs-lookup"><span data-stu-id="071e2-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="071e2-124">之後，SYSMON 會隨機播放線條寬度。</span><span class="sxs-lookup"><span data-stu-id="071e2-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="071e2-125">如需詳細資訊，請參閱 [**CounterItem。**](counteritem-color.md)</span><span class="sxs-lookup"><span data-stu-id="071e2-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="071e2-126">若要指定純色以外的 [**線條樣式**](counteritem-linestyle.md) ，寬度必須為1。</span><span class="sxs-lookup"><span data-stu-id="071e2-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="071e2-127">如果您指定大於1的值，並指定非實線樣式，SYSMON 會忽略指定的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="071e2-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="071e2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="071e2-128">Requirements</span></span>



| <span data-ttu-id="071e2-129">需求</span><span class="sxs-lookup"><span data-stu-id="071e2-129">Requirement</span></span> | <span data-ttu-id="071e2-130">值</span><span class="sxs-lookup"><span data-stu-id="071e2-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="071e2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="071e2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="071e2-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071e2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="071e2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="071e2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="071e2-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071e2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="071e2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="071e2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="071e2-136"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="071e2-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071e2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="071e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071e2-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="071e2-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





