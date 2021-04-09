---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 類別
description: MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 類別是用來抓取 StartTime 和 StopTime 中存在的記錄。
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 類別
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024627"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="7ff51-105">MDM \_ 報告 \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 類別</span><span class="sxs-lookup"><span data-stu-id="7ff51-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="7ff51-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7ff51-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ff51-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7ff51-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ff51-108">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** 類別是用來抓取 StartTime 和 StopTime 中存在的記錄。</span><span class="sxs-lookup"><span data-stu-id="7ff51-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="7ff51-109">StartTime 和 StopTime 是以 ISO 8601 格式表示。</span><span class="sxs-lookup"><span data-stu-id="7ff51-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="7ff51-110">如果未指定 StartTime 和 StopTime，則會將值轉譯為第一個現有或最後一個現有的時間。</span><span class="sxs-lookup"><span data-stu-id="7ff51-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="7ff51-111">以下是其他可能的案例：</span><span class="sxs-lookup"><span data-stu-id="7ff51-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="7ff51-112">如果未指定 StartTime 和 StopTime，則會傳回所有現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="7ff51-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="7ff51-113">如果指定了 StopTime，但未指定 StartTime，則會傳回 StopTime 之前存在的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="7ff51-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="7ff51-114">如果指定 StartTime，但是未指定 StopTime，則會傳回從 StartTime 中存在的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="7ff51-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="7ff51-115">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7ff51-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff51-116">語法</span><span class="sxs-lookup"><span data-stu-id="7ff51-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="7ff51-117">成員</span><span class="sxs-lookup"><span data-stu-id="7ff51-117">Members</span></span>

<span data-ttu-id="7ff51-118">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ff51-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="7ff51-119">屬性</span><span class="sxs-lookup"><span data-stu-id="7ff51-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ff51-120">屬性</span><span class="sxs-lookup"><span data-stu-id="7ff51-120">Properties</span></span>

<span data-ttu-id="7ff51-121">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7ff51-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ff51-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ff51-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ff51-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ff51-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ff51-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ff51-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ff51-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="7ff51-127">此類別的字串為 "RetrieveByTimeRange"。</span><span class="sxs-lookup"><span data-stu-id="7ff51-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="7ff51-128">記錄</span><span class="sxs-lookup"><span data-stu-id="7ff51-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ff51-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ff51-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ff51-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7ff51-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ff51-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7ff51-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ff51-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ff51-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7ff51-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="7ff51-136">此類別的字串為 "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="7ff51-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="7ff51-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="7ff51-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ff51-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ff51-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ff51-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="7ff51-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7ff51-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ff51-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ff51-143">型別</span><span class="sxs-lookup"><span data-stu-id="7ff51-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff51-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ff51-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ff51-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ff51-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ff51-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ff51-146">Requirements</span></span>



| <span data-ttu-id="7ff51-147">需求</span><span class="sxs-lookup"><span data-stu-id="7ff51-147">Requirement</span></span> | <span data-ttu-id="7ff51-148">值</span><span class="sxs-lookup"><span data-stu-id="7ff51-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff51-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ff51-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff51-150">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ff51-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ff51-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ff51-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff51-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="7ff51-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="7ff51-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="7ff51-153">Namespace</span></span><br/>                | <span data-ttu-id="7ff51-154">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7ff51-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="7ff51-155">MOF</span><span class="sxs-lookup"><span data-stu-id="7ff51-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ff51-156"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ff51-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="7ff51-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff51-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff51-158"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff51-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

