---
title: MDM_SharedPC 類別
description: MDM \_ >sharedpc 類別是用來設定共用電腦使用方式的設定。
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- MDM_SharedPC 類別
- MDM_SharedPC 類別，描述
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024626"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="3a511-105">MDM \_ >sharedpc 類別</span><span class="sxs-lookup"><span data-stu-id="3a511-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="3a511-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3a511-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3a511-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3a511-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3a511-108">MDM \_ >sharedpc 類別是用來設定共用電腦使用方式的設定。</span><span class="sxs-lookup"><span data-stu-id="3a511-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="3a511-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3a511-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a511-110">語法</span><span class="sxs-lookup"><span data-stu-id="3a511-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="3a511-111">成員</span><span class="sxs-lookup"><span data-stu-id="3a511-111">Members</span></span>

<span data-ttu-id="3a511-112">**MDM \_ >sharedpc** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3a511-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="3a511-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3a511-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a511-114">屬性</span><span class="sxs-lookup"><span data-stu-id="3a511-114">Properties</span></span>

<span data-ttu-id="3a511-115">**MDM \_ >sharedpc** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3a511-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3a511-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="3a511-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-119">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a511-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-123">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="3a511-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-125">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-127">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="3a511-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-131">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="3a511-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-135">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="3a511-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-139">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="3a511-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-143">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="3a511-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a511-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a511-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a511-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a511-147">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a511-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a511-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="3a511-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a511-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-151">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="3a511-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a511-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-155">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="3a511-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-157">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-159">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="3a511-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-161">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-163">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="3a511-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3a511-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3a511-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a511-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a511-167">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a511-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a511-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="3a511-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-169">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-171">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="3a511-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-173">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-175">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-176">SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="3a511-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-177">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-179">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="3a511-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-181">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3a511-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-183">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="3a511-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="3a511-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a511-185">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a511-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a511-186">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3a511-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a511-187">如需詳細資訊，請參閱 [>SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp)。</span><span class="sxs-lookup"><span data-stu-id="3a511-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a511-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a511-188">Requirements</span></span>



| <span data-ttu-id="3a511-189">需求</span><span class="sxs-lookup"><span data-stu-id="3a511-189">Requirement</span></span> | <span data-ttu-id="3a511-190">值</span><span class="sxs-lookup"><span data-stu-id="3a511-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a511-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a511-191">Minimum supported client</span></span><br/> | <span data-ttu-id="3a511-192">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a511-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a511-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a511-193">Minimum supported server</span></span><br/> | <span data-ttu-id="3a511-194">都不支援</span><span class="sxs-lookup"><span data-stu-id="3a511-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3a511-195">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a511-195">Namespace</span></span><br/>                | <span data-ttu-id="3a511-196">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3a511-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3a511-197">MOF</span><span class="sxs-lookup"><span data-stu-id="3a511-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a511-198"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a511-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a511-199">DLL</span><span class="sxs-lookup"><span data-stu-id="3a511-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a511-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a511-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

