---
title: SystemMonitor. GetLogViewRange 方法
description: 抓取用來從記錄檔中取出計數器值的開始日期。
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- GetLogViewRange 方法 SysMon
- GetLogViewRange 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，GetLogViewRange 方法
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508588"
---
# <a name="systemmonitorgetlogviewrange-method"></a><span data-ttu-id="b48c1-106">SystemMonitor. GetLogViewRange 方法</span><span class="sxs-lookup"><span data-stu-id="b48c1-106">SystemMonitor.GetLogViewRange method</span></span>

<span data-ttu-id="b48c1-107">抓取用來從記錄檔中取出計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="b48c1-107">Retrieves the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="b48c1-108">Syntax</span></span>


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="b48c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="b48c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48c1-110">*StartTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b48c1-111">用來從記錄檔中取出計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="b48c1-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="b48c1-112">*StopTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-112">*StopTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b48c1-113">用來從記錄檔中取出計數器值的結束日期。</span><span class="sxs-lookup"><span data-stu-id="b48c1-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b48c1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b48c1-114">Return value</span></span>

<span data-ttu-id="b48c1-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b48c1-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b48c1-116">備註</span><span class="sxs-lookup"><span data-stu-id="b48c1-116">Remarks</span></span>

<span data-ttu-id="b48c1-117">SYSMON 會從開始和停止日期內的記錄檔抓取計數器值（含）。</span><span class="sxs-lookup"><span data-stu-id="b48c1-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="b48c1-118">使用這個方法與存取 [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) 和 [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="b48c1-118">Using this method is the same as accessing the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48c1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b48c1-119">Requirements</span></span>



| <span data-ttu-id="b48c1-120">需求</span><span class="sxs-lookup"><span data-stu-id="b48c1-120">Requirement</span></span> | <span data-ttu-id="b48c1-121">值</span><span class="sxs-lookup"><span data-stu-id="b48c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b48c1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b48c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b48c1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b48c1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b48c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b48c1-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b48c1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b48c1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b48c1-127"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b48c1-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48c1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b48c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48c1-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b48c1-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="b48c1-130">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="b48c1-130">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





