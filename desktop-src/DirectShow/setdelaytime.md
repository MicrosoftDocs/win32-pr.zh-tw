---
description: SetDelayTime 方法會設定與 MSWebDVD 物件相關聯的工具提示延遲時間。
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467408"
---
# <a name="setdelaytime"></a><span data-ttu-id="07dc6-103">SetDelayTime</span><span class="sxs-lookup"><span data-stu-id="07dc6-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="07dc6-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="07dc6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="07dc6-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="07dc6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="07dc6-106">`SetDelayTime`方法會設定與 **MSWebDVD** 物件相關聯的工具提示延遲時間。</span><span class="sxs-lookup"><span data-stu-id="07dc6-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="07dc6-107">參數</span><span class="sxs-lookup"><span data-stu-id="07dc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07dc6-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span><span class="sxs-lookup"><span data-stu-id="07dc6-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="07dc6-109">將延遲的類型指定為整數。</span><span class="sxs-lookup"><span data-stu-id="07dc6-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="07dc6-110">值</span><span class="sxs-lookup"><span data-stu-id="07dc6-110">Value</span></span> | <span data-ttu-id="07dc6-111">描述</span><span class="sxs-lookup"><span data-stu-id="07dc6-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07dc6-112">-1</span><span class="sxs-lookup"><span data-stu-id="07dc6-112">-1</span></span>    | <span data-ttu-id="07dc6-113">若要將 autopop 延遲時間重設為預設值，請將 *iNewVal* 設定為-1。</span><span class="sxs-lookup"><span data-stu-id="07dc6-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="07dc6-114">0</span><span class="sxs-lookup"><span data-stu-id="07dc6-114">0</span></span>     | <span data-ttu-id="07dc6-115">設定當指標在工具周框內為固定時，工具提示視窗保持可見的時間長度。</span><span class="sxs-lookup"><span data-stu-id="07dc6-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="07dc6-116">1</span><span class="sxs-lookup"><span data-stu-id="07dc6-116">1</span></span>     | <span data-ttu-id="07dc6-117">設定在顯示工具提示視窗之前，指標必須保持在工具周框內保持靜止的時間長度。</span><span class="sxs-lookup"><span data-stu-id="07dc6-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="07dc6-118">2</span><span class="sxs-lookup"><span data-stu-id="07dc6-118">2</span></span>     | <span data-ttu-id="07dc6-119">設定當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間長度。</span><span class="sxs-lookup"><span data-stu-id="07dc6-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="07dc6-120">3</span><span class="sxs-lookup"><span data-stu-id="07dc6-120">3</span></span>     | <span data-ttu-id="07dc6-121">將所有延遲時間設定為預設比例。</span><span class="sxs-lookup"><span data-stu-id="07dc6-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="07dc6-122">Autopop 時間是初始時間的10倍，而 reshow 時間是初始時間的一到五倍。</span><span class="sxs-lookup"><span data-stu-id="07dc6-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="07dc6-123">如果設定此旗標，請使用正值 iNewVal 來指定初始時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="07dc6-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="07dc6-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span><span class="sxs-lookup"><span data-stu-id="07dc6-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="07dc6-125">指定以毫秒為單位的延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="07dc6-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="07dc6-126">值</span><span class="sxs-lookup"><span data-stu-id="07dc6-126">Value</span></span>                    | <span data-ttu-id="07dc6-127">描述</span><span class="sxs-lookup"><span data-stu-id="07dc6-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="07dc6-128">-1</span><span class="sxs-lookup"><span data-stu-id="07dc6-128">-1</span></span>                       | <span data-ttu-id="07dc6-129">將 *iDelayType* 中指定的延遲設定為其預設值</span><span class="sxs-lookup"><span data-stu-id="07dc6-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="07dc6-130">任何其他負數值</span><span class="sxs-lookup"><span data-stu-id="07dc6-130">any other negative value</span></span> | <span data-ttu-id="07dc6-131">將所有延遲類型設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="07dc6-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07dc6-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="07dc6-132">Return Value</span></span>

<span data-ttu-id="07dc6-133">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="07dc6-133">No return value.</span></span>

 

 



