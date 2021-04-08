---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別
description: MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02 類別是用來抓取 StartTime 和 StopTime 中存在的記錄。
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685548"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="e8bcb-105">MDM \_ 報告 \_ SecurityAuditing01 \_ RetrieveByTimeRange02 類別</span><span class="sxs-lookup"><span data-stu-id="e8bcb-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="e8bcb-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8bcb-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e8bcb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8bcb-108">**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別用來抓取 starttime 和 StopTime 中的記錄檔。 STARTTIME 和 StopTime 是以 ISO 8601 格式表示。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="e8bcb-109">如果未指定 StartTime 和 StopTime，則會將值轉譯為第一個現有或最後一個現有的時間。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="e8bcb-110">以下是其他可能的案例：</span><span class="sxs-lookup"><span data-stu-id="e8bcb-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="e8bcb-111">如果未指定 StartTime 和 StopTime，則會傳回所有現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="e8bcb-112">如果指定了 StopTime，但未指定 StartTime，則會傳回 StopTime 之前存在的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="e8bcb-113">如果指定 StartTime，但是未指定 StopTime，則會傳回從 StartTime 中存在的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="e8bcb-114">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bcb-115">語法</span><span class="sxs-lookup"><span data-stu-id="e8bcb-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="e8bcb-116">成員</span><span class="sxs-lookup"><span data-stu-id="e8bcb-116">Members</span></span>

<span data-ttu-id="e8bcb-117">**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e8bcb-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="e8bcb-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e8bcb-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8bcb-119">屬性</span><span class="sxs-lookup"><span data-stu-id="e8bcb-119">Properties</span></span>

<span data-ttu-id="e8bcb-120">**MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8bcb-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8bcb-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8bcb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8bcb-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e8bcb-125">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="e8bcb-126">此類別的字串為 "RetrieveByTimeRange"。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="e8bcb-127">記錄</span><span class="sxs-lookup"><span data-stu-id="e8bcb-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8bcb-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e8bcb-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8bcb-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8bcb-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8bcb-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8bcb-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e8bcb-134">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e8bcb-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="e8bcb-135">此類別的字串為 "./Vendor/MSFT/SecurityAuditing"</span><span class="sxs-lookup"><span data-stu-id="e8bcb-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="e8bcb-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="e8bcb-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8bcb-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e8bcb-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8bcb-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="e8bcb-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8bcb-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8bcb-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8bcb-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e8bcb-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8bcb-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8bcb-142">Requirements</span></span>



| <span data-ttu-id="e8bcb-143">需求</span><span class="sxs-lookup"><span data-stu-id="e8bcb-143">Requirement</span></span> | <span data-ttu-id="e8bcb-144">值</span><span class="sxs-lookup"><span data-stu-id="e8bcb-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bcb-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8bcb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e8bcb-146">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8bcb-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e8bcb-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8bcb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e8bcb-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="e8bcb-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e8bcb-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="e8bcb-149">Namespace</span></span><br/>                | <span data-ttu-id="e8bcb-150">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e8bcb-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="e8bcb-151">MOF</span><span class="sxs-lookup"><span data-stu-id="e8bcb-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8bcb-152"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8bcb-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="e8bcb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bcb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8bcb-154"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bcb-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

