---
title: CounterItem. GetDataAt 方法
description: 從圖形中的特定點抓取指定的計數器值。
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- GetDataAt 方法 SysMon
- GetDataAt 方法 SysMon，CounterItem 物件
- CounterItem 物件 SysMon，GetDataAt 方法
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508671"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="8b9f5-106">CounterItem. GetDataAt 方法</span><span class="sxs-lookup"><span data-stu-id="8b9f5-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="8b9f5-107">從圖形中的特定點抓取指定的計數器值。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9f5-108">語法</span><span class="sxs-lookup"><span data-stu-id="8b9f5-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="8b9f5-109">參數</span><span class="sxs-lookup"><span data-stu-id="8b9f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b9f5-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b9f5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f5-111">您要取得其值之圖形點的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="8b9f5-112">有效值的範圍是從0到 ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1) 。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="8b9f5-113">*哪* \[ 一個在\]</span><span class="sxs-lookup"><span data-stu-id="8b9f5-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f5-114">要抓取的計數器數值型別，例如，在圖形視窗中顯示的計數器平均值。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="8b9f5-115">如需可能的值，請參閱 [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="8b9f5-116">*變異* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b9f5-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f5-117">已取出的計數器值。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b9f5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b9f5-118">Return value</span></span>

<span data-ttu-id="8b9f5-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8b9f5-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b9f5-120">備註</span><span class="sxs-lookup"><span data-stu-id="8b9f5-120">Remarks</span></span>

<span data-ttu-id="8b9f5-121">只有在下列情況下才使用這個方法</span><span class="sxs-lookup"><span data-stu-id="8b9f5-121">Use this method only if</span></span>

-   <span data-ttu-id="8b9f5-122">[**SystemMonitor**](systemmonitor-displaytype.md) 會設定為 sysmonLineGraph</span><span class="sxs-lookup"><span data-stu-id="8b9f5-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="8b9f5-123">[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 設定為 SysmonLogFiles 或 sysmonSqlLog</span><span class="sxs-lookup"><span data-stu-id="8b9f5-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9f5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b9f5-124">Requirements</span></span>



| <span data-ttu-id="8b9f5-125">需求</span><span class="sxs-lookup"><span data-stu-id="8b9f5-125">Requirement</span></span> | <span data-ttu-id="8b9f5-126">值</span><span class="sxs-lookup"><span data-stu-id="8b9f5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9f5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b9f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9f5-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b9f5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b9f5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b9f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9f5-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b9f5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b9f5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8b9f5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b9f5-132"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8b9f5-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9f5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b9f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9f5-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="8b9f5-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="8b9f5-135">**CounterItem.GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="8b9f5-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="8b9f5-136">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="8b9f5-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





