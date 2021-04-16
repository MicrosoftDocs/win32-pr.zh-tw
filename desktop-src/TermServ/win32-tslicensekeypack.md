---
title: Win32_TSLicenseKeyPack 類別
description: 提供用來查看和安裝遠端桌面服務授權金鑰套件的方法和屬性。
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack 類別遠端桌面服務
- Win32_TSLicenseKeyPack 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508324"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="c3564-105">Win32 \_ TSLicenseKeyPack 類別</span><span class="sxs-lookup"><span data-stu-id="c3564-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c3564-106">提供用來查看和安裝遠端桌面服務授權金鑰套件的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="c3564-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3564-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3564-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="c3564-108">成員</span><span class="sxs-lookup"><span data-stu-id="c3564-108">Members</span></span>

<span data-ttu-id="c3564-109">**Win32 \_ TSLicenseKeyPack** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c3564-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="c3564-110">方法</span><span class="sxs-lookup"><span data-stu-id="c3564-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3564-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c3564-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3564-112">方法</span><span class="sxs-lookup"><span data-stu-id="c3564-112">Methods</span></span>

<span data-ttu-id="c3564-113">**Win32 \_ TSLicenseKeyPack** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c3564-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="c3564-114">方法</span><span class="sxs-lookup"><span data-stu-id="c3564-114">Method</span></span>                                                                                                        | <span data-ttu-id="c3564-115">描述</span><span class="sxs-lookup"><span data-stu-id="c3564-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3564-116">**ConvertLicenses**</span><span class="sxs-lookup"><span data-stu-id="c3564-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="c3564-117">轉換目前金鑰套件中的授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="c3564-118">**ImportAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="c3564-119">從另一部遠端桌面授權伺服器匯入，這是透過授權合約購買的遠端桌面服務授權金鑰套件，並會透過網際網路自動連接來驗證金鑰套件授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="c3564-120">**ImportLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="c3564-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="c3564-121">從另一部遠端桌面授權伺服器匯入，這是使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="c3564-122">**ImportOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="c3564-123">從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="c3564-124">**ImportRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="c3564-125">從另一部遠端桌面授權伺服器匯入，這是透過零售通路購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c3564-126">**InstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="c3564-127">安裝透過合約授權購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="c3564-128">**InstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="c3564-129">安裝遠端桌面服務授權金鑰套件，此套件會使用透過網際網路或電話所收到的授權金鑰包識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3564-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="c3564-130">**InstallOpenLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="c3564-131">安裝透過 open license 合約購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="c3564-132">**InstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="c3564-133">安裝透過零售商店購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="c3564-134">**ReinstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="c3564-135">重新安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="c3564-136">**ReinstallLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="c3564-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="c3564-137">重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c3564-138">**ReinstallOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="c3564-139">重新安裝 Open License 遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="c3564-140">**ReinstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="c3564-141">重新安裝透過零售通路購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="c3564-142">**RemoveLicensesWithIdCount**</span><span class="sxs-lookup"><span data-stu-id="c3564-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="c3564-143">從指定的金鑰套件中移除指定的遠端桌面服務授權數目。</span><span class="sxs-lookup"><span data-stu-id="c3564-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="c3564-144">**UninstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c3564-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="c3564-145">卸載遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="c3564-146">**UninstallLicenseKeyPackWithId**</span><span class="sxs-lookup"><span data-stu-id="c3564-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="c3564-147">使用指定的金鑰套件識別碼卸載遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="c3564-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="c3564-148">屬性</span><span class="sxs-lookup"><span data-stu-id="c3564-148">Properties</span></span>

<span data-ttu-id="c3564-149">**Win32 \_ TSLicenseKeyPack** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c3564-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3564-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="c3564-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3564-153">限定詞： [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ( "0"、"1"、"2"、"3" ) 、 [**BITVALUES**](/windows/desktop/WmiSdk/standard-qualifiers) ( "RD 會話"、"VDI 會話"、"CALISTA"、"vdi 合作夥伴" ) </span><span class="sxs-lookup"><span data-stu-id="c3564-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="c3564-154">TS 授權金鑰套件存取權限的辨識符號</span><span class="sxs-lookup"><span data-stu-id="c3564-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="c3564-155">**AvailableLicenses**</span><span class="sxs-lookup"><span data-stu-id="c3564-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-158">遠端桌面服務授權金鑰套件中的可用授權數總計。</span><span class="sxs-lookup"><span data-stu-id="c3564-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-159">**說明**</span><span class="sxs-lookup"><span data-stu-id="c3564-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3564-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-162">遠端桌面服務授權金鑰套件的描述。</span><span class="sxs-lookup"><span data-stu-id="c3564-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="c3564-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-164">資料類型： **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="c3564-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-166">遠端桌面服務授權金鑰套件的到期日。</span><span class="sxs-lookup"><span data-stu-id="c3564-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-167">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="c3564-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-170">遠端桌面服務授權金鑰套件中已發行的授權總數。</span><span class="sxs-lookup"><span data-stu-id="c3564-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-171">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="c3564-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3564-174">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3564-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3564-175">遠端桌面服務授權金鑰套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3564-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-176">**KeyPackType**</span><span class="sxs-lookup"><span data-stu-id="c3564-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-179">遠端桌面授權伺服器的金鑰套件類型。</span><span class="sxs-lookup"><span data-stu-id="c3564-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="c3564-180">值</span><span class="sxs-lookup"><span data-stu-id="c3564-180">Value</span></span> | <span data-ttu-id="c3564-181">描述</span><span class="sxs-lookup"><span data-stu-id="c3564-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="c3564-182">0</span><span class="sxs-lookup"><span data-stu-id="c3564-182">0</span></span> | <span data-ttu-id="c3564-183">遠端桌面服務的授權金鑰包類型未知。</span><span class="sxs-lookup"><span data-stu-id="c3564-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="c3564-184">1</span><span class="sxs-lookup"><span data-stu-id="c3564-184">1</span></span> | <span data-ttu-id="c3564-185">遠端桌面服務授權金鑰套件類型是零售版購買。</span><span class="sxs-lookup"><span data-stu-id="c3564-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="c3564-186">2</span><span class="sxs-lookup"><span data-stu-id="c3564-186">2</span></span> | <span data-ttu-id="c3564-187">遠端桌面服務的授權金鑰包類型為大量購買。</span><span class="sxs-lookup"><span data-stu-id="c3564-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="c3564-188">3</span><span class="sxs-lookup"><span data-stu-id="c3564-188">3</span></span> | <span data-ttu-id="c3564-189">遠端桌面服務授權金鑰套件類型是並行授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="c3564-190">4</span><span class="sxs-lookup"><span data-stu-id="c3564-190">4</span></span> | <span data-ttu-id="c3564-191">遠端桌面服務的授權金鑰包類型為暫時性。</span><span class="sxs-lookup"><span data-stu-id="c3564-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="c3564-192">5</span><span class="sxs-lookup"><span data-stu-id="c3564-192">5</span></span> | <span data-ttu-id="c3564-193">遠端桌面服務授權金鑰套件類型是 open 授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="c3564-194">6</span><span class="sxs-lookup"><span data-stu-id="c3564-194">6</span></span> | <span data-ttu-id="c3564-195">不支援。</span><span class="sxs-lookup"><span data-stu-id="c3564-195">Not supported.</span></span> |

<span data-ttu-id="c3564-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="c3564-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-199">遠端桌面服務授權金鑰套件的產品類型。</span><span class="sxs-lookup"><span data-stu-id="c3564-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="c3564-200">值</span><span class="sxs-lookup"><span data-stu-id="c3564-200">Value</span></span> | <span data-ttu-id="c3564-201">描述</span><span class="sxs-lookup"><span data-stu-id="c3564-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="c3564-202">0</span><span class="sxs-lookup"><span data-stu-id="c3564-202">0</span></span> | <span data-ttu-id="c3564-203">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="c3564-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="c3564-204">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="c3564-205">1</span><span class="sxs-lookup"><span data-stu-id="c3564-205">1</span></span> | <span data-ttu-id="c3564-206">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="c3564-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="c3564-207">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="c3564-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="c3564-208">2</span><span class="sxs-lookup"><span data-stu-id="c3564-208">2</span></span> | <span data-ttu-id="c3564-209">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="c3564-209">This product type is not valid.</span></span> |

<span data-ttu-id="c3564-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="c3564-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3564-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-213">遠端桌面服務授權金鑰套件的產品版本。</span><span class="sxs-lookup"><span data-stu-id="c3564-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="c3564-214">值</span><span class="sxs-lookup"><span data-stu-id="c3564-214">Value</span></span> | <span data-ttu-id="c3564-215">描述</span><span class="sxs-lookup"><span data-stu-id="c3564-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="c3564-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="c3564-216">"Windows Server 2012"</span></span> | <span data-ttu-id="c3564-217">此授權僅支援執行 Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3564-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="c3564-218">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="c3564-218">"Windows Server 7"</span></span> | <span data-ttu-id="c3564-219">此授權僅支援執行 Windows Server 2008 R2 或 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3564-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="c3564-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="c3564-220">"Windows Server 2008"</span></span> | <span data-ttu-id="c3564-221">此金鑰套件只支援執行 Windows Server 2008 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c3564-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="c3564-222">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="c3564-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-223">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-225">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3564-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="c3564-226">值</span><span class="sxs-lookup"><span data-stu-id="c3564-226">Value</span></span> | <span data-ttu-id="c3564-227">描述</span><span class="sxs-lookup"><span data-stu-id="c3564-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="c3564-228">0</span><span class="sxs-lookup"><span data-stu-id="c3564-228">0</span></span> | <span data-ttu-id="c3564-229">不支援</span><span class="sxs-lookup"><span data-stu-id="c3564-229">Not supported</span></span> |
| <span data-ttu-id="c3564-230">1</span><span class="sxs-lookup"><span data-stu-id="c3564-230">1</span></span> | <span data-ttu-id="c3564-231">不支援</span><span class="sxs-lookup"><span data-stu-id="c3564-231">Not supported</span></span> |
| <span data-ttu-id="c3564-232">2</span><span class="sxs-lookup"><span data-stu-id="c3564-232">2</span></span> | <span data-ttu-id="c3564-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3564-233">Windows Server 2008</span></span> |
| <span data-ttu-id="c3564-234">3</span><span class="sxs-lookup"><span data-stu-id="c3564-234">3</span></span> | <span data-ttu-id="c3564-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3564-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="c3564-236">4</span><span class="sxs-lookup"><span data-stu-id="c3564-236">4</span></span> | <span data-ttu-id="c3564-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c3564-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="c3564-238">5</span><span class="sxs-lookup"><span data-stu-id="c3564-238">5</span></span> | <span data-ttu-id="c3564-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c3564-239">Windows Server 2016</span></span> |
| <span data-ttu-id="c3564-240">6</span><span class="sxs-lookup"><span data-stu-id="c3564-240">6</span></span> | <span data-ttu-id="c3564-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="c3564-241">Windows Server 2019</span></span> |

<span data-ttu-id="c3564-242">**TotalLicenses**</span><span class="sxs-lookup"><span data-stu-id="c3564-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-243">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3564-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-245">遠端桌面服務授權金鑰套件中的授權總數。</span><span class="sxs-lookup"><span data-stu-id="c3564-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c3564-246">**TypeAndModel**</span><span class="sxs-lookup"><span data-stu-id="c3564-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3564-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3564-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3564-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3564-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3564-249">TS 授權金鑰套件類型和模型的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="c3564-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="c3564-250">範例： VDI 每個裝置訂用帳戶授權，TS 每個使用者 CAL</span><span class="sxs-lookup"><span data-stu-id="c3564-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3564-251">備註</span><span class="sxs-lookup"><span data-stu-id="c3564-251">Remarks</span></span>

<span data-ttu-id="c3564-252">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="c3564-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="c3564-253">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c3564-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c3564-254">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c3564-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c3564-255">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c3564-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c3564-256">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c3564-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3564-257">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3564-257">Requirements</span></span>



| <span data-ttu-id="c3564-258">需求</span><span class="sxs-lookup"><span data-stu-id="c3564-258">Requirement</span></span> | <span data-ttu-id="c3564-259">值</span><span class="sxs-lookup"><span data-stu-id="c3564-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3564-260">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3564-260">Minimum supported client</span></span><br/> | <span data-ttu-id="c3564-261">都不支援</span><span class="sxs-lookup"><span data-stu-id="c3564-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c3564-262">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3564-262">Minimum supported server</span></span><br/> | <span data-ttu-id="c3564-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3564-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c3564-264">命名空間</span><span class="sxs-lookup"><span data-stu-id="c3564-264">Namespace</span></span><br/>                | <span data-ttu-id="c3564-265">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c3564-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c3564-266">MOF</span><span class="sxs-lookup"><span data-stu-id="c3564-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3564-267"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3564-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3564-268">DLL</span><span class="sxs-lookup"><span data-stu-id="c3564-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3564-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3564-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3564-270">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3564-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3564-271">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="c3564-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="c3564-272">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="c3564-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="c3564-273">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="c3564-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="c3564-274">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c3564-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

