---
title: SystemMonitor 屬性
description: 抓取或設定用來繪製效能計數器資料圖形的圖表類型。
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- DisplayType 屬性 SysMon
- DisplayType 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，DisplayType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103835"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="56eec-106">SystemMonitor 屬性</span><span class="sxs-lookup"><span data-stu-id="56eec-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="56eec-107">抓取或設定用來繪製效能計數器資料圖形的圖表類型。</span><span class="sxs-lookup"><span data-stu-id="56eec-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="56eec-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="56eec-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56eec-109">語法</span><span class="sxs-lookup"><span data-stu-id="56eec-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="56eec-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="56eec-110">Property value</span></span>

<span data-ttu-id="56eec-111">用來繪製效能計數器資料圖形的圖表類型。</span><span class="sxs-lookup"><span data-stu-id="56eec-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="56eec-112">如需可能的值，請參閱 [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)。</span><span class="sxs-lookup"><span data-stu-id="56eec-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="56eec-113">例外狀況</span><span class="sxs-lookup"><span data-stu-id="56eec-113">Exceptions</span></span>



| <span data-ttu-id="56eec-114">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="56eec-114">Exception type</span></span>               | <span data-ttu-id="56eec-115">條件</span><span class="sxs-lookup"><span data-stu-id="56eec-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="56eec-116">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="56eec-116">**System.ArgumentException**</span></span> | <span data-ttu-id="56eec-117">指定的圖形或報表值無效。</span><span class="sxs-lookup"><span data-stu-id="56eec-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="56eec-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="56eec-118">Requirements</span></span>



| <span data-ttu-id="56eec-119">需求</span><span class="sxs-lookup"><span data-stu-id="56eec-119">Requirement</span></span> | <span data-ttu-id="56eec-120">值</span><span class="sxs-lookup"><span data-stu-id="56eec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56eec-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56eec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56eec-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56eec-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="56eec-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56eec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56eec-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56eec-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56eec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56eec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56eec-126"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="56eec-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56eec-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56eec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56eec-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="56eec-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





