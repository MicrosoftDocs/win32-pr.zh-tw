---
description: 允許啟動時間點度量收集的規格，並指定定期資料收集的慣用取樣間隔時間。
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: CIM_MetricService 類別的 ControlSampleTimes 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979178"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="3a868-103">CIM MetricService 類別的 ControlSampleTimes 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3a868-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="3a868-104">允許啟動時間點度量收集的規格，並指定定期資料收集的慣用取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="3a868-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="3a868-105">每次啟動其他計量的取樣時，都可以使用這個方法所指定的設定。</span><span class="sxs-lookup"><span data-stu-id="3a868-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a868-106">語法</span><span class="sxs-lookup"><span data-stu-id="3a868-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="3a868-107">參數</span><span class="sxs-lookup"><span data-stu-id="3a868-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a868-108">*StartSampleTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a868-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a868-109">開始計量取樣的時間點。</span><span class="sxs-lookup"><span data-stu-id="3a868-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="3a868-110">99990101000000.000000 + 000 的值應該指出在下一次同步處理至全小時時，應開始取樣。</span><span class="sxs-lookup"><span data-stu-id="3a868-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="3a868-111">當午夜模數取樣間隔（以秒為單位）等於0之後，取樣會同步處理至全小時。</span><span class="sxs-lookup"><span data-stu-id="3a868-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="3a868-112">*PreferredSampleInterval* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a868-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a868-113">慣用的取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="3a868-113">Preferred sample interval time.</span></span> <span data-ttu-id="3a868-114">若要取得相關計量，建議您選擇取樣間隔，方法是3600模數取樣間隔時間（秒）等於0。</span><span class="sxs-lookup"><span data-stu-id="3a868-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="3a868-115">CIM 計量服務的責任是要決定是否接受要求的取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="3a868-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="3a868-116">CIM 用戶端可以藉由取出相關的 BaseMetricDefinition 實例並檢查 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的內容，來檢查計量提供者是否接受要求的取樣間隔時間。**SampleInterval** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3a868-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="3a868-117">*RestartGathering* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a868-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a868-118">**TRUE** 表示要求收集與度量服務相關聯的所有計量，並使用此方法呼叫重新開機。</span><span class="sxs-lookup"><span data-stu-id="3a868-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a868-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a868-119">Return value</span></span>

<span data-ttu-id="3a868-120">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a868-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3a868-121">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="3a868-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a868-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="3a868-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a868-123">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="3a868-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a868-124">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3a868-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a868-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="3a868-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3a868-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a868-126">Requirements</span></span>



| <span data-ttu-id="3a868-127">需求</span><span class="sxs-lookup"><span data-stu-id="3a868-127">Requirement</span></span> | <span data-ttu-id="3a868-128">值</span><span class="sxs-lookup"><span data-stu-id="3a868-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a868-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a868-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a868-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3a868-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3a868-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a868-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a868-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3a868-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3a868-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a868-133">Namespace</span></span><br/>                | <span data-ttu-id="3a868-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a868-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a868-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3a868-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a868-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3a868-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a868-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3a868-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a868-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a868-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a868-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a868-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a868-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="3a868-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




