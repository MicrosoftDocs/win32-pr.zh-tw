---
title: SystemMonitor DataSourceType 屬性
description: 抓取或設定效能計數器資料的來源。
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- DataSourceType 屬性 SysMon
- DataSourceType 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、DataSourceType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025311"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="191ae-106">SystemMonitor：:D ataSourceType 屬性</span><span class="sxs-lookup"><span data-stu-id="191ae-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="191ae-107">抓取或設定效能計數器資料的來源。</span><span class="sxs-lookup"><span data-stu-id="191ae-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="191ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="191ae-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="191ae-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="191ae-109">Property value</span></span>

<span data-ttu-id="191ae-110">效能計數器資料的來源。</span><span class="sxs-lookup"><span data-stu-id="191ae-110">Source of the performance counter data.</span></span> <span data-ttu-id="191ae-111">如需可能的值，請參閱 [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants)。</span><span class="sxs-lookup"><span data-stu-id="191ae-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="191ae-112">例外狀況</span><span class="sxs-lookup"><span data-stu-id="191ae-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="191ae-113">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="191ae-113">Exception type</span></span></th>
<th><span data-ttu-id="191ae-114">條件</span><span class="sxs-lookup"><span data-stu-id="191ae-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="191ae-115"><strong>System. ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="191ae-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="191ae-116">您可能會因為下列其中一個原因而收到此例外狀況：</span><span class="sxs-lookup"><span data-stu-id="191ae-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="191ae-117">指定的資料來源值無效。</span><span class="sxs-lookup"><span data-stu-id="191ae-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="191ae-118">如果資料來源是記錄檔，則 SYSMON 找不到其中一個指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="191ae-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="191ae-119">Err 值為0xC0000BD1。</span><span class="sxs-lookup"><span data-stu-id="191ae-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="191ae-120">備註</span><span class="sxs-lookup"><span data-stu-id="191ae-120">Remarks</span></span>

<span data-ttu-id="191ae-121">**在 Windows Vista 之前：** 如果這個屬性的值設定為 sysmonLogFiles，您就無法從 [**記錄檔集合**](systemmonitor-logfiles.md) 加入或移除記錄檔。</span><span class="sxs-lookup"><span data-stu-id="191ae-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="191ae-122">只有在建立或修改記錄檔集合之後，才將這個屬性的值設定為 sysmonLogFiles。</span><span class="sxs-lookup"><span data-stu-id="191ae-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="191ae-123">此外，如果這個屬性的值不能設定為 sysmonSqlLog，則無法修改 [**SqlDsnName**](systemmonitor-sqldsnname.md) 和 [**SqlLogSetName**](systemmonitor-sqllogsetname.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="191ae-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="191ae-124">在修改伺服器和資料庫名稱之後，請只將這個屬性的值設定為 sysmonSqlLog。</span><span class="sxs-lookup"><span data-stu-id="191ae-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="191ae-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="191ae-125">Requirements</span></span>



| <span data-ttu-id="191ae-126">需求</span><span class="sxs-lookup"><span data-stu-id="191ae-126">Requirement</span></span> | <span data-ttu-id="191ae-127">值</span><span class="sxs-lookup"><span data-stu-id="191ae-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="191ae-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="191ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="191ae-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="191ae-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="191ae-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="191ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="191ae-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="191ae-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="191ae-132">DLL</span><span class="sxs-lookup"><span data-stu-id="191ae-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="191ae-133"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="191ae-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191ae-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="191ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191ae-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="191ae-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





