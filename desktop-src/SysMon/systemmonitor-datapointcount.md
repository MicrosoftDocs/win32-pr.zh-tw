---
title: SystemMonitor. DataPointCount 屬性
description: 抓取或設定線條圖形中顯示的資料點數目。
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- DataPointCount 屬性 SysMon
- DataPointCount 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，DataPointCount 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934147"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="02555-106">SystemMonitor. DataPointCount 屬性</span><span class="sxs-lookup"><span data-stu-id="02555-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="02555-107">抓取或設定線條圖形中顯示的資料點數目。</span><span class="sxs-lookup"><span data-stu-id="02555-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="02555-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="02555-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="02555-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="02555-109">Property value</span></span>

<span data-ttu-id="02555-110">折線圖中顯示的資料點數目。</span><span class="sxs-lookup"><span data-stu-id="02555-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="02555-111">預設值為100資料點。</span><span class="sxs-lookup"><span data-stu-id="02555-111">The default value is 100 data points.</span></span> <span data-ttu-id="02555-112">值的有效範圍是2到1000。</span><span class="sxs-lookup"><span data-stu-id="02555-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="02555-113">備註</span><span class="sxs-lookup"><span data-stu-id="02555-113">Remarks</span></span>

<span data-ttu-id="02555-114">只有在 [**SystemMonitor DataSourceType**](systemmonitor-datasourcetype.md) 為 **sysmonCurrentActivity** 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="02555-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02555-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="02555-115">Requirements</span></span>



| <span data-ttu-id="02555-116">需求</span><span class="sxs-lookup"><span data-stu-id="02555-116">Requirement</span></span> | <span data-ttu-id="02555-117">值</span><span class="sxs-lookup"><span data-stu-id="02555-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02555-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02555-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02555-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02555-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02555-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02555-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02555-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02555-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02555-122">DLL</span><span class="sxs-lookup"><span data-stu-id="02555-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02555-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="02555-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





