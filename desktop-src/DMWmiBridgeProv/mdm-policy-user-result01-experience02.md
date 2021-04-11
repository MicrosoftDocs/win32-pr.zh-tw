---
title: MDM_Policy_User_Result01_Experience02 類別
description: MDM \_ Policy \_ User \_ Result01 \_ Experience02 類別代表可用的體驗原則。
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- MDM_Policy_User_Result01_Experience02 類別
- MDM_Policy_User_Result01_Experience02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843627"
---
# <a name="mdm_policy_user_result01_experience02-class"></a><span data-ttu-id="5573b-105">MDM \_ 原則 \_ 使用者 \_ Result01 \_ Experience02 類別</span><span class="sxs-lookup"><span data-stu-id="5573b-105">MDM\_Policy\_User\_Result01\_Experience02 class</span></span>

<span data-ttu-id="5573b-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5573b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5573b-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5573b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5573b-108">**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別代表可用的體驗原則。</span><span class="sxs-lookup"><span data-stu-id="5573b-108">The **MDM\_Policy\_User\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="5573b-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5573b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5573b-110">語法</span><span class="sxs-lookup"><span data-stu-id="5573b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="5573b-111">成員</span><span class="sxs-lookup"><span data-stu-id="5573b-111">Members</span></span>

<span data-ttu-id="5573b-112">**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5573b-112">The **MDM\_Policy\_User\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="5573b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5573b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5573b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5573b-114">Properties</span></span>

<span data-ttu-id="5573b-115">**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5573b-115">The **MDM\_Policy\_User\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5573b-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="5573b-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="5573b-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="5573b-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="5573b-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="5573b-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="5573b-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5573b-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="5573b-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5573b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5573b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5573b-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5573b-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5573b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5573b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5573b-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5573b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5573b-141">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5573b-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="5573b-142">針對此類別，字串為「經驗」。</span><span class="sxs-lookup"><span data-stu-id="5573b-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="5573b-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5573b-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5573b-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5573b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5573b-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5573b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5573b-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5573b-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5573b-147">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5573b-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="5573b-148">此類別的字串為 "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="5573b-148">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5573b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="5573b-149">Requirements</span></span>



| <span data-ttu-id="5573b-150">需求</span><span class="sxs-lookup"><span data-stu-id="5573b-150">Requirement</span></span> | <span data-ttu-id="5573b-151">值</span><span class="sxs-lookup"><span data-stu-id="5573b-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5573b-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5573b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5573b-153">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5573b-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5573b-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5573b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5573b-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="5573b-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="5573b-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="5573b-156">Namespace</span></span><br/>                | <span data-ttu-id="5573b-157">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="5573b-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="5573b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="5573b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5573b-159"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="5573b-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="5573b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="5573b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5573b-161"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5573b-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

