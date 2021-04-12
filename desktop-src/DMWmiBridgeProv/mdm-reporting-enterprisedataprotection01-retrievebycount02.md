---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 類別
description: MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02 類別是用來從 StartTime 取出指定數目的記錄。
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 類別
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464348"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="f9af2-105">MDM \_ 報告 \_ EnterpriseDataProtection01 \_ RetrieveByCount02 類別</span><span class="sxs-lookup"><span data-stu-id="f9af2-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="f9af2-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="f9af2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f9af2-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="f9af2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f9af2-108">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** 類別是用來從 StartTime 取出指定數目的記錄。</span><span class="sxs-lookup"><span data-stu-id="f9af2-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="f9af2-109">StartTime 是以 ISO 8601 格式表示。</span><span class="sxs-lookup"><span data-stu-id="f9af2-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="f9af2-110">您可以設定 LogCount 和 StartTime 來設定所需的記錄檔數目。</span><span class="sxs-lookup"><span data-stu-id="f9af2-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="f9af2-111">如果總數目記錄檔小於 LogCount，則會傳回指定的記錄數目（或更少）。</span><span class="sxs-lookup"><span data-stu-id="f9af2-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="f9af2-112">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9af2-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9af2-113">語法</span><span class="sxs-lookup"><span data-stu-id="f9af2-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="f9af2-114">成員</span><span class="sxs-lookup"><span data-stu-id="f9af2-114">Members</span></span>

<span data-ttu-id="f9af2-115">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9af2-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="f9af2-116">屬性</span><span class="sxs-lookup"><span data-stu-id="f9af2-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9af2-117">屬性</span><span class="sxs-lookup"><span data-stu-id="f9af2-117">Properties</span></span>

<span data-ttu-id="f9af2-118">**MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9af2-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9af2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f9af2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9af2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9af2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9af2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9af2-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9af2-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f9af2-124">此類別的字串為 "RetrieveByCount"。</span><span class="sxs-lookup"><span data-stu-id="f9af2-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="f9af2-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="f9af2-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f9af2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9af2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f9af2-128">記錄</span><span class="sxs-lookup"><span data-stu-id="f9af2-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9af2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9af2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9af2-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f9af2-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9af2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9af2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9af2-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9af2-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f9af2-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="f9af2-136">此類別的字串為 "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="f9af2-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="f9af2-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="f9af2-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9af2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9af2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f9af2-140">型別</span><span class="sxs-lookup"><span data-stu-id="f9af2-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9af2-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f9af2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9af2-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9af2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9af2-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9af2-143">Requirements</span></span>



| <span data-ttu-id="f9af2-144">需求</span><span class="sxs-lookup"><span data-stu-id="f9af2-144">Requirement</span></span> | <span data-ttu-id="f9af2-145">值</span><span class="sxs-lookup"><span data-stu-id="f9af2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9af2-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9af2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f9af2-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9af2-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f9af2-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9af2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f9af2-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="f9af2-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f9af2-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9af2-150">Namespace</span></span><br/>                | <span data-ttu-id="f9af2-151">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f9af2-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f9af2-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f9af2-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9af2-153"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9af2-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f9af2-154">DLL</span><span class="sxs-lookup"><span data-stu-id="f9af2-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9af2-155"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9af2-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

