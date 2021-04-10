---
title: MDM_Policy_Result01_Power02 類別
description: MDM \_ Policy \_ Result01 \_ Power02 類別代表電源原則。
ms.assetid: 1458228f-f442-4fd4-b402-e0a4c06ecaa5
keywords:
- MDM_Policy_Result01_Power02 類別
- MDM_Policy_Result01_Power02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Power02
- MDM_Policy_Result01_Power02.InstanceID
- MDM_Policy_Result01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91635811e876500cb4d3df792067b1eba3d861b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934039"
---
# <a name="mdm_policy_result01_power02-class"></a><span data-ttu-id="b655e-105">MDM \_ 原則 \_ Result01 \_ Power02 類別</span><span class="sxs-lookup"><span data-stu-id="b655e-105">MDM\_Policy\_Result01\_Power02 class</span></span>

<span data-ttu-id="b655e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b655e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b655e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b655e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b655e-108">MDM \_ Policy \_ Result01 \_ Power02 類別代表電源原則。</span><span class="sxs-lookup"><span data-stu-id="b655e-108">The MDM\_Policy\_Result01\_Power02 class represents the power policies.</span></span>

<span data-ttu-id="b655e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b655e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b655e-110">語法</span><span class="sxs-lookup"><span data-stu-id="b655e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="b655e-111">成員</span><span class="sxs-lookup"><span data-stu-id="b655e-111">Members</span></span>

<span data-ttu-id="b655e-112">**MDM \_ Policy \_ Result01 \_ Power02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b655e-112">The **MDM\_Policy\_Result01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="b655e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b655e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b655e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b655e-114">Properties</span></span>

<span data-ttu-id="b655e-115">**MDM \_ Policy \_ Result01 \_ Power02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b655e-115">The **MDM\_Policy\_Result01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b655e-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="b655e-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="b655e-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="b655e-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="b655e-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="b655e-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b655e-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b655e-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b655e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b655e-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b655e-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b655e-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b655e-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b655e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b655e-138">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b655e-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="b655e-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="b655e-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="b655e-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b655e-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="b655e-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b655e-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b655e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b655e-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b655e-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b655e-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="b655e-151">Requirements</span></span>



| <span data-ttu-id="b655e-152">需求</span><span class="sxs-lookup"><span data-stu-id="b655e-152">Requirement</span></span> | <span data-ttu-id="b655e-153">值</span><span class="sxs-lookup"><span data-stu-id="b655e-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b655e-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b655e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b655e-155">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b655e-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b655e-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b655e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b655e-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="b655e-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b655e-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="b655e-158">Namespace</span></span><br/>                | <span data-ttu-id="b655e-159">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b655e-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b655e-160">MOF</span><span class="sxs-lookup"><span data-stu-id="b655e-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b655e-161"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b655e-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b655e-162">DLL</span><span class="sxs-lookup"><span data-stu-id="b655e-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b655e-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b655e-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

