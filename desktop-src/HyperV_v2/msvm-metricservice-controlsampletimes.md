---
description: 設定控制項取樣時間。
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Msvm_MetricService 類別的 ControlSampleTimes 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192670"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="a74e3-103">Msvm MetricService 類別的 ControlSampleTimes 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a74e3-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="a74e3-104">設定控制項取樣時間。</span><span class="sxs-lookup"><span data-stu-id="a74e3-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="a74e3-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="a74e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="a74e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74e3-107">*StartSampleTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a74e3-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74e3-108">開始計量取樣的時間點。</span><span class="sxs-lookup"><span data-stu-id="a74e3-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="a74e3-109">99990101000000.000000 + 000 的值應該指出在下一次同步處理至全小時時，應開始取樣。</span><span class="sxs-lookup"><span data-stu-id="a74e3-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="a74e3-110">當午夜模數取樣間隔（以秒為單位）等於0之後，取樣會同步處理至全小時。</span><span class="sxs-lookup"><span data-stu-id="a74e3-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a74e3-111">*PreferredSampleInterval* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a74e3-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74e3-112">慣用的取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="a74e3-112">Preferred sample interval time.</span></span> <span data-ttu-id="a74e3-113">若要取得相關計量，建議您選擇取樣間隔，方法是3600模數取樣間隔時間（秒）等於0。</span><span class="sxs-lookup"><span data-stu-id="a74e3-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="a74e3-114">CIM 計量服務的責任是要決定是否接受要求的取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="a74e3-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="a74e3-115">CIM 用戶端可以藉由取出相關的 BaseMetricDefinition 實例並檢查 "CIM \_ BaseMetricDefinition. SampleInterval" 屬性的內容，來檢查計量提供者是否接受要求的取樣間隔時間。</span><span class="sxs-lookup"><span data-stu-id="a74e3-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="a74e3-116">*RestartGathering* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a74e3-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a74e3-117">布林值，當設為 TRUE 時，要求收集與計量服務相關聯的所有計量都會透過此方法呼叫重新開機。</span><span class="sxs-lookup"><span data-stu-id="a74e3-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74e3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a74e3-118">Return value</span></span>

<span data-ttu-id="a74e3-119">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="a74e3-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="a74e3-120">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="a74e3-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a74e3-121">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a74e3-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a74e3-122">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="a74e3-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a74e3-123">**方法保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a74e3-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a74e3-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a74e3-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a74e3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a74e3-125">Requirements</span></span>



| <span data-ttu-id="a74e3-126">需求</span><span class="sxs-lookup"><span data-stu-id="a74e3-126">Requirement</span></span> | <span data-ttu-id="a74e3-127">值</span><span class="sxs-lookup"><span data-stu-id="a74e3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a74e3-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a74e3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a74e3-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a74e3-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a74e3-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a74e3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a74e3-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a74e3-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a74e3-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="a74e3-132">Namespace</span></span><br/>                | <span data-ttu-id="a74e3-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a74e3-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a74e3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a74e3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a74e3-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a74e3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a74e3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a74e3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74e3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a74e3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a74e3-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a74e3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74e3-139">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="a74e3-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




