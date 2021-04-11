---
title: SystemMonitor SqlDsnName 屬性
description: 抓取或設定 (DSN) 的 ODBC 資料來源名稱。
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- SqlDsnName 屬性 SysMon
- SqlDsnName 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、SqlDsnName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383826"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="4d731-106">SystemMonitor：： SqlDsnName 屬性</span><span class="sxs-lookup"><span data-stu-id="4d731-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="4d731-107">抓取或設定 (DSN) 的 ODBC 資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="4d731-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d731-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d731-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="4d731-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="4d731-109">Property value</span></span>

<span data-ttu-id="4d731-110">指向包含正確 Perfmon 資料表之資料庫的 ODBC 資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="4d731-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="4d731-111">格式為 SQL： DSN。</span><span class="sxs-lookup"><span data-stu-id="4d731-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d731-112">備註</span><span class="sxs-lookup"><span data-stu-id="4d731-112">Remarks</span></span>

<span data-ttu-id="4d731-113">您必須使用 Perfmon MMC 嵌入式管理單元來產生 SQL 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4d731-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="4d731-114">計數器記錄檔位於 **效能記錄檔及警示** 下。</span><span class="sxs-lookup"><span data-stu-id="4d731-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="4d731-115">若要指定 SQL 記錄檔，請以滑鼠右鍵按一下您所建立的記錄檔，然後從功能表中選取 [ **屬性** ]。</span><span class="sxs-lookup"><span data-stu-id="4d731-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="4d731-116">在 [**記錄** 檔] 屬性頁上，從 [**記錄檔案類型**] 下拉式清單方塊中選取 **SQL Database** 。</span><span class="sxs-lookup"><span data-stu-id="4d731-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="4d731-117">**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 的值設定為 [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法修改此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d731-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="4d731-118">您必須先指定名稱，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonSqlLog**。</span><span class="sxs-lookup"><span data-stu-id="4d731-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d731-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d731-119">Requirements</span></span>



| <span data-ttu-id="4d731-120">需求</span><span class="sxs-lookup"><span data-stu-id="4d731-120">Requirement</span></span> | <span data-ttu-id="4d731-121">值</span><span class="sxs-lookup"><span data-stu-id="4d731-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d731-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d731-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d731-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d731-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4d731-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d731-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d731-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d731-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d731-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4d731-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d731-127"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4d731-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d731-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d731-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d731-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="4d731-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="4d731-130">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="4d731-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





