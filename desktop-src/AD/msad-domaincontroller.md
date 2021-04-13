---
title: MSAD_DomainController 類別
description: 代表執行 WMI 提供者的網域控制站 (DC) 。
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController 類別 Active Directory
- MSAD_DomainController 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465396"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="ab33f-105">MSAD 的 [ \_ 控制器] 類別</span><span class="sxs-lookup"><span data-stu-id="ab33f-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="ab33f-106">代表執行 WMI 提供者的網域控制站 (DC) 。</span><span class="sxs-lookup"><span data-stu-id="ab33f-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab33f-107">語法</span><span class="sxs-lookup"><span data-stu-id="ab33f-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="ab33f-108">成員</span><span class="sxs-lookup"><span data-stu-id="ab33f-108">Members</span></span>

<span data-ttu-id="ab33f-109">MSAD 的 [ **\_ 控制器** ] 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ab33f-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="ab33f-110">方法</span><span class="sxs-lookup"><span data-stu-id="ab33f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab33f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ab33f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab33f-112">方法</span><span class="sxs-lookup"><span data-stu-id="ab33f-112">Methods</span></span>

<span data-ttu-id="ab33f-113">MSAD 的 [ **\_ 控制器** ] 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ab33f-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="ab33f-114">方法</span><span class="sxs-lookup"><span data-stu-id="ab33f-114">Method</span></span>                                                 | <span data-ttu-id="ab33f-115">描述</span><span class="sxs-lookup"><span data-stu-id="ab33f-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab33f-116">**ExecuteKCC**</span><span class="sxs-lookup"><span data-stu-id="ab33f-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="ab33f-117">叫用知識一致性檢查程式，以確認複寫拓撲。</span><span class="sxs-lookup"><span data-stu-id="ab33f-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ab33f-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ab33f-118">Properties</span></span>

<span data-ttu-id="ab33f-119">MSAD 的 [ **\_ 控制器** ] 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ab33f-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab33f-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="ab33f-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab33f-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-123">取得伺服器物件的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="ab33f-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="ab33f-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab33f-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab33f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-128">取得 [**NTDS DSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件的 X. 500 路徑。</span><span class="sxs-lookup"><span data-stu-id="ab33f-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-129">**IsAdvertisingToLocator**</span><span class="sxs-lookup"><span data-stu-id="ab33f-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab33f-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-132">取得值，這個值會指出 DC 上的定位器服務是否正確地廣告。</span><span class="sxs-lookup"><span data-stu-id="ab33f-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="ab33f-133">如果 DC 上的定位器服務正確通告，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab33f-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-134">**IsGC**</span><span class="sxs-lookup"><span data-stu-id="ab33f-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab33f-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-137">取得值，這個值會指出 DC 是否為通用類別目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="ab33f-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="ab33f-138">如果 DC 是通用類別目錄伺服器，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab33f-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-139">**IsNextRIDPoolAvailable**</span><span class="sxs-lookup"><span data-stu-id="ab33f-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab33f-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-142">取得值，這個值會指出 DC 是否已取得另一個 RID 集區。</span><span class="sxs-lookup"><span data-stu-id="ab33f-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="ab33f-143">**如果 DC** 已取得另一個 RID 集區，而且即使目前的 rid 集區已用盡，此 dc 上的 rid 的配置仍可繼續。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab33f-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-144">**IsRegisteredInDNS**</span><span class="sxs-lookup"><span data-stu-id="ab33f-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab33f-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-147">取得值，這個值會指出是否已在 DNS 中正確註冊 DC。</span><span class="sxs-lookup"><span data-stu-id="ab33f-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="ab33f-148">如果 DC 已在 DNS 中正確註冊，則 **為 TRUE** 。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab33f-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-149">**IsSysVolReady**</span><span class="sxs-lookup"><span data-stu-id="ab33f-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ab33f-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-152">取得值，這個值會指出 SysVol 是否已正確發佈。</span><span class="sxs-lookup"><span data-stu-id="ab33f-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="ab33f-153">如果 SysVol 已正確發行，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab33f-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-154">**NTDsaGUID**</span><span class="sxs-lookup"><span data-stu-id="ab33f-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab33f-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-157">取得與設定容器中的 [**NTDS DSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件相關聯的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ab33f-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="ab33f-158">**NTDS DSA** 物件代表伺服器上的 ACTIVE DIRECTORY 網域 Service DSA 進程。</span><span class="sxs-lookup"><span data-stu-id="ab33f-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-159">**PercentOfRIDsLeft**</span><span class="sxs-lookup"><span data-stu-id="ab33f-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab33f-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-162">取得保留在此 DC 上目前 RID 集區中的 Rid 百分比。</span><span class="sxs-lookup"><span data-stu-id="ab33f-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-163">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="ab33f-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ab33f-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-166">取得 DC 所在的網站。</span><span class="sxs-lookup"><span data-stu-id="ab33f-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-167">**TimeOfOldestReplAdd**</span><span class="sxs-lookup"><span data-stu-id="ab33f-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-168">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab33f-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-170">取得仍在此網域控制站上的佇列中最舊的複寫新增作業的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab33f-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-171">**TimeOfOldestReplDel**</span><span class="sxs-lookup"><span data-stu-id="ab33f-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-172">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab33f-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-174">取得仍在此網域控制站上的佇列中之最舊複寫刪除作業的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab33f-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-175">**TimeOfOldestReplMod**</span><span class="sxs-lookup"><span data-stu-id="ab33f-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-176">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab33f-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-178">取得在此網域控制站上仍在佇列中之最舊複寫修改作業的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab33f-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-179">**TimeOfOldestReplSync**</span><span class="sxs-lookup"><span data-stu-id="ab33f-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-180">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab33f-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-182">取得仍在此網域控制站上的佇列中最舊複寫同步作業的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab33f-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="ab33f-183">**TimeOfOldestReplUpdRefs**</span><span class="sxs-lookup"><span data-stu-id="ab33f-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab33f-184">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ab33f-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab33f-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab33f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab33f-186">取得仍在此網域控制站上的佇列中之最舊複寫更新作業的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ab33f-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab33f-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab33f-187">Requirements</span></span>



| <span data-ttu-id="ab33f-188">需求</span><span class="sxs-lookup"><span data-stu-id="ab33f-188">Requirement</span></span> | <span data-ttu-id="ab33f-189">值</span><span class="sxs-lookup"><span data-stu-id="ab33f-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab33f-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab33f-190">Minimum supported client</span></span><br/> | <span data-ttu-id="ab33f-191">都不支援</span><span class="sxs-lookup"><span data-stu-id="ab33f-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ab33f-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab33f-192">Minimum supported server</span></span><br/> | <span data-ttu-id="ab33f-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab33f-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab33f-194">命名空間</span><span class="sxs-lookup"><span data-stu-id="ab33f-194">Namespace</span></span><br/>                | <span data-ttu-id="ab33f-195">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ab33f-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="ab33f-196">MOF</span><span class="sxs-lookup"><span data-stu-id="ab33f-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab33f-197"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab33f-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab33f-198">DLL</span><span class="sxs-lookup"><span data-stu-id="ab33f-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab33f-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab33f-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

