---
title: CounterItem。 Color 屬性
description: 抓取或設定用來繪製計數器值的色彩。
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- 色彩屬性 SysMon
- Color 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，色彩屬性
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686012"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="de5b4-106">CounterItem。 Color 屬性</span><span class="sxs-lookup"><span data-stu-id="de5b4-106">CounterItem.Color property</span></span>

<span data-ttu-id="de5b4-107">抓取或設定用來繪製計數器值的色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="de5b4-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="de5b4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5b4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de5b4-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="de5b4-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="de5b4-110">Property value</span></span>

<span data-ttu-id="de5b4-111">用來繪製計數器值的色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5b4-112">備註</span><span class="sxs-lookup"><span data-stu-id="de5b4-112">Remarks</span></span>

<span data-ttu-id="de5b4-113">如果您未指定要使用的色彩，SYSMON 會選取前十六個計數器的色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="de5b4-114">如果您指定十六個以上的計數器，SYSMON 將會重複使用前十六個計數器的相同色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="de5b4-115">為了協助區分計數器，SYSMON 會將每個16個計數器的每個倍數所使用的 [**線條樣式**](counteritem-linestyle.md) 變更為第一個80計數器。</span><span class="sxs-lookup"><span data-stu-id="de5b4-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="de5b4-116">例如，前十六個計數器使用實線樣式，接下來的十六個使用虛線樣式，依此類推。</span><span class="sxs-lookup"><span data-stu-id="de5b4-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="de5b4-117">然後 SYSMON 會將計數器 81-96 的 [**線條寬度**](counteritem-width.md) 設定為2，並將計數器 96-112 設定為3。</span><span class="sxs-lookup"><span data-stu-id="de5b4-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="de5b4-118">如果集合包含112個以上的計數器，計數器將會包含重複的色彩、線條樣式和寬度值。</span><span class="sxs-lookup"><span data-stu-id="de5b4-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="de5b4-119">**在 Windows Vista 之前：** 如果您未指定要使用的色彩，SYSMON 會選取前十六個計數器的色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="de5b4-120">如果您指定十六個以上的計數器，SYSMON 將會重複使用前十六個計數器的相同色彩。</span><span class="sxs-lookup"><span data-stu-id="de5b4-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="de5b4-121">為了協助區分計數器，SYSMON 會增加接收相同色彩指派之前三個計數器的 [**行寬**](counteritem-width.md) 。</span><span class="sxs-lookup"><span data-stu-id="de5b4-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="de5b4-122">如果有三個以上的計數器使用相同的色彩，SYSMON 會隨機播放要用於計數器的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="de5b4-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5b4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="de5b4-123">Requirements</span></span>



| <span data-ttu-id="de5b4-124">需求</span><span class="sxs-lookup"><span data-stu-id="de5b4-124">Requirement</span></span> | <span data-ttu-id="de5b4-125">值</span><span class="sxs-lookup"><span data-stu-id="de5b4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de5b4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de5b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de5b4-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de5b4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="de5b4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de5b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de5b4-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de5b4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de5b4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="de5b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de5b4-131"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="de5b4-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5b4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de5b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5b4-133">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="de5b4-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





