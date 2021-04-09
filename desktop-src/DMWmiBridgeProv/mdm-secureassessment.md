---
title: MDM_SecureAssessment 類別
description: MDM \_ SecureAssessmentclass 可用來提供安全評定瀏覽器的設定資訊。
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- MDM_SecureAssessment 類別
- MDM_SecureAssessment 類別，描述
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933945"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="30420-105">MDM \_ SecureAssessment 類別</span><span class="sxs-lookup"><span data-stu-id="30420-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="30420-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="30420-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="30420-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="30420-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="30420-108">**MDM \_ SecureAssessment** 類別可用來提供安全評定瀏覽器的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="30420-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="30420-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="30420-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="30420-110">語法</span><span class="sxs-lookup"><span data-stu-id="30420-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="30420-111">成員</span><span class="sxs-lookup"><span data-stu-id="30420-111">Members</span></span>

<span data-ttu-id="30420-112">**MDM \_ SecureAssessment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30420-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="30420-113">屬性</span><span class="sxs-lookup"><span data-stu-id="30420-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30420-114">屬性</span><span class="sxs-lookup"><span data-stu-id="30420-114">Properties</span></span>

<span data-ttu-id="30420-115">**MDM \_ SecureAssessment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="30420-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="30420-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="30420-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="30420-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30420-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30420-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="30420-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="30420-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="30420-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30420-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30420-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30420-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="30420-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="30420-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30420-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="30420-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30420-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="30420-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="30420-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="30420-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="30420-127">此類別的字串為 "SecureAssessment"。</span><span class="sxs-lookup"><span data-stu-id="30420-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="30420-128">LaunchURI</span><span class="sxs-lookup"><span data-stu-id="30420-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="30420-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30420-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30420-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30420-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="30420-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="30420-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30420-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="30420-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30420-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="30420-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="30420-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="30420-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="30420-136">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="30420-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="30420-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="30420-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="30420-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30420-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30420-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="30420-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="30420-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="30420-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="30420-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30420-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="30420-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30420-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="30420-143">Requirements</span></span>



| <span data-ttu-id="30420-144">需求</span><span class="sxs-lookup"><span data-stu-id="30420-144">Requirement</span></span> | <span data-ttu-id="30420-145">值</span><span class="sxs-lookup"><span data-stu-id="30420-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30420-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30420-146">Minimum supported client</span></span><br/> | <span data-ttu-id="30420-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30420-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="30420-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30420-148">Minimum supported server</span></span><br/> | <span data-ttu-id="30420-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="30420-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="30420-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="30420-150">Namespace</span></span><br/>                | <span data-ttu-id="30420-151">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="30420-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="30420-152">MOF</span><span class="sxs-lookup"><span data-stu-id="30420-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30420-153"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="30420-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="30420-154">DLL</span><span class="sxs-lookup"><span data-stu-id="30420-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30420-155"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30420-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

