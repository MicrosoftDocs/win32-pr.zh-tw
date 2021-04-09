---
title: SystemMonitor. ScaleToFit 方法
description: 調整計數器值以納入圖形中。
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- ScaleToFit 方法 SysMon
- ScaleToFit 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ScaleToFit 方法
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685810"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="273ca-106">SystemMonitor. ScaleToFit 方法</span><span class="sxs-lookup"><span data-stu-id="273ca-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="273ca-107">調整計數器值以納入圖形中。</span><span class="sxs-lookup"><span data-stu-id="273ca-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="273ca-108">語法</span><span class="sxs-lookup"><span data-stu-id="273ca-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="273ca-109">參數</span><span class="sxs-lookup"><span data-stu-id="273ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273ca-110">*selectedCountersOnly* \[在\]</span><span class="sxs-lookup"><span data-stu-id="273ca-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ca-111">True 表示只調整選取的計數器;否則，則為 false 以調整所有計數器。</span><span class="sxs-lookup"><span data-stu-id="273ca-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273ca-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="273ca-112">Return value</span></span>

<span data-ttu-id="273ca-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="273ca-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="273ca-114">備註</span><span class="sxs-lookup"><span data-stu-id="273ca-114">Remarks</span></span>

<span data-ttu-id="273ca-115">此方法會清除圖表視圖。</span><span class="sxs-lookup"><span data-stu-id="273ca-115">This method will clear the graph view.</span></span> <span data-ttu-id="273ca-116">如果資料來源是記錄檔，SYSMON 就會使用針對每個計數器指定的縮放比例來重繪圖形，或在資料來源為即時活動時開始繪製新計數器值。</span><span class="sxs-lookup"><span data-stu-id="273ca-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="273ca-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="273ca-117">Requirements</span></span>



| <span data-ttu-id="273ca-118">需求</span><span class="sxs-lookup"><span data-stu-id="273ca-118">Requirement</span></span> | <span data-ttu-id="273ca-119">值</span><span class="sxs-lookup"><span data-stu-id="273ca-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="273ca-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="273ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="273ca-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="273ca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="273ca-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="273ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="273ca-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="273ca-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="273ca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="273ca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="273ca-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="273ca-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="273ca-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="273ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273ca-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="273ca-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="273ca-128">**CounterItem.ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="273ca-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="273ca-129">**CounterItem。已選取**</span><span class="sxs-lookup"><span data-stu-id="273ca-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





