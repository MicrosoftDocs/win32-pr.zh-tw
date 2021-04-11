---
title: SystemMonitor SqlLogSetName 屬性
description: 抓取或設定記錄集的易記名稱。
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- SqlLogSetName 屬性 SysMon
- SqlLogSetName 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、SqlLogSetName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024551"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="550fb-106">SystemMonitor：： SqlLogSetName 屬性</span><span class="sxs-lookup"><span data-stu-id="550fb-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="550fb-107">抓取或設定記錄集的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="550fb-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="550fb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="550fb-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="550fb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="550fb-109">Property value</span></span>

<span data-ttu-id="550fb-110">記錄集的易記名稱，對應至 SQL database 中包含二進位或文字資料的單一記錄檔。</span><span class="sxs-lookup"><span data-stu-id="550fb-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="550fb-111">備註</span><span class="sxs-lookup"><span data-stu-id="550fb-111">Remarks</span></span>

<span data-ttu-id="550fb-112">**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 的值設定為 sysmonSqlLog，您就無法修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="550fb-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="550fb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="550fb-113">Requirements</span></span>



| <span data-ttu-id="550fb-114">需求</span><span class="sxs-lookup"><span data-stu-id="550fb-114">Requirement</span></span> | <span data-ttu-id="550fb-115">值</span><span class="sxs-lookup"><span data-stu-id="550fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="550fb-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="550fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="550fb-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="550fb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="550fb-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="550fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="550fb-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="550fb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="550fb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="550fb-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="550fb-121"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="550fb-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550fb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="550fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550fb-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="550fb-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="550fb-124">**SystemMonitor.SqlDsnName**</span><span class="sxs-lookup"><span data-stu-id="550fb-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





