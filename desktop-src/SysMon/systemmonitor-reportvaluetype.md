---
title: SystemMonitor. ReportValueType 屬性
description: 抓取或設定值，這個值會決定長條圖和報表檢視是否會圖形化取樣間隔期間所取樣的最後一個值，或取樣中的計算值，例如平均或最小計數器值。
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- ReportValueType 屬性 SysMon
- ReportValueType 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ReportValueType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934334"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="9d961-106">SystemMonitor. ReportValueType 屬性</span><span class="sxs-lookup"><span data-stu-id="9d961-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="9d961-107">抓取或設定值，這個值會決定長條圖和報表檢視是否會圖形化取樣間隔期間所取樣的最後一個值，或取樣中的計算值，例如平均或最小計數器值。</span><span class="sxs-lookup"><span data-stu-id="9d961-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="9d961-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9d961-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d961-109">語法</span><span class="sxs-lookup"><span data-stu-id="9d961-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="9d961-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9d961-110">Property value</span></span>

<span data-ttu-id="9d961-111">判斷長條圖和報表檢視是否會在取樣間隔期間，或取樣間隔中的計算值，繪製出最後取樣的值。</span><span class="sxs-lookup"><span data-stu-id="9d961-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="9d961-112">如需可能的值，請參閱 [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants)。</span><span class="sxs-lookup"><span data-stu-id="9d961-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d961-113">備註</span><span class="sxs-lookup"><span data-stu-id="9d961-113">Remarks</span></span>

<span data-ttu-id="9d961-114">如果 [**SystemMonitor**](systemmonitor-displaytype.md)未 [**DisplayTypeConstants.sysMonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)或 **DisplayTypeConstants.sysmonReport**，SYSMON 會忽略此值，並使用 [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) 。</span><span class="sxs-lookup"><span data-stu-id="9d961-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d961-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d961-115">Requirements</span></span>



| <span data-ttu-id="9d961-116">需求</span><span class="sxs-lookup"><span data-stu-id="9d961-116">Requirement</span></span> | <span data-ttu-id="9d961-117">值</span><span class="sxs-lookup"><span data-stu-id="9d961-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d961-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d961-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d961-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d961-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9d961-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d961-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d961-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d961-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d961-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9d961-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d961-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9d961-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d961-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d961-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d961-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="9d961-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





