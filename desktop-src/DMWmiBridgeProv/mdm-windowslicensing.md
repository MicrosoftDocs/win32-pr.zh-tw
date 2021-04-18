---
title: MDM_WindowsLicensing 類別
description: MDM \_ WindowsLicensing 類別是針對授權相關的管理案例所設計。
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966106"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="a743e-105">MDM \_ WindowsLicensing 類別</span><span class="sxs-lookup"><span data-stu-id="a743e-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="a743e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a743e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a743e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a743e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a743e-108">**MDM \_ WindowsLicensing** 類別是針對授權相關的管理案例所設計。</span><span class="sxs-lookup"><span data-stu-id="a743e-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="a743e-109">目前的範圍僅限於 Windows 10 桌面和行動裝置的版本升級，例如 Windows 10 企業版的 Windows 10 專業版。</span><span class="sxs-lookup"><span data-stu-id="a743e-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="a743e-110">此外，此 CSP 也提供啟用或變更 Windows 10 桌面裝置之產品金鑰的功能。</span><span class="sxs-lookup"><span data-stu-id="a743e-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="a743e-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a743e-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a743e-112">語法</span><span class="sxs-lookup"><span data-stu-id="a743e-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="a743e-113">成員</span><span class="sxs-lookup"><span data-stu-id="a743e-113">Members</span></span>

<span data-ttu-id="a743e-114">**MDM \_ WindowsLicensing** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a743e-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="a743e-115">方法</span><span class="sxs-lookup"><span data-stu-id="a743e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="a743e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a743e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a743e-117">方法</span><span class="sxs-lookup"><span data-stu-id="a743e-117">Methods</span></span>

<span data-ttu-id="a743e-118">**MDM \_ WindowsLicensing** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a743e-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a743e-119">方法</span><span class="sxs-lookup"><span data-stu-id="a743e-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a743e-120">描述</span><span class="sxs-lookup"><span data-stu-id="a743e-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a743e-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="a743e-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a743e-122">安裝 Windows 10 桌面裝置的產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="a743e-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="a743e-123">不會重新開機。</span><span class="sxs-lookup"><span data-stu-id="a743e-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a743e-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="a743e-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a743e-125">方法，檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="a743e-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a743e-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="a743e-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a743e-127">針對 Windows 10 行動裝置的版本升級提供授權。</span><span class="sxs-lookup"><span data-stu-id="a743e-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a743e-128">此升級程式不需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="a743e-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="a743e-129">日期類型是 XML。</span><span class="sxs-lookup"><span data-stu-id="a743e-129">The date type is XML.</span></span><br/> <span data-ttu-id="a743e-130">支援的作業為執行。</span><span class="sxs-lookup"><span data-stu-id="a743e-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="a743e-131">XML 授權檔案內容必須經過正確的轉義 (也就是說，它不應該只是複製的 XML) ，否則 Windows 10 行動裝置上的版本升級將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a743e-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="a743e-132">如需有關 XML 授權檔案正確地轉義的詳細資訊，請參閱 <a href="https://www.w3.org/TR/xml/">W3C XML 規格</a>的2.4 節。XML 授權檔案是從 Microsoft 大量授權服務中心取得的。</span><span class="sxs-lookup"><span data-stu-id="a743e-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="a743e-133">您的組織必須具有 Microsoft 的大量授權合約，才能存取入口網站。</span><span class="sxs-lookup"><span data-stu-id="a743e-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="a743e-134">以下是透過 MDM 或布建套件使用此節點時的有效版本升級路徑：</span><span class="sxs-lookup"><span data-stu-id="a743e-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="a743e-135">Windows 10 Mobileto Windows 10 行動裝置企業版</span><span class="sxs-lookup"><span data-stu-id="a743e-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a743e-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="a743e-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="a743e-137">觸發裝置以取得產品金鑰，並升級用戶端的版本。</span><span class="sxs-lookup"><span data-stu-id="a743e-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a743e-138">此升級程式需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="a743e-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="a743e-139">支援的作業為執行。</span><span class="sxs-lookup"><span data-stu-id="a743e-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="a743e-140">將產品金鑰從 MDM 伺服器推送到使用者的裝置時， <strong>changepk.exe</strong> 使用產品金鑰執行。</span><span class="sxs-lookup"><span data-stu-id="a743e-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="a743e-141">完成之後，就會向使用者顯示通知，指出有新版本的 Windows 10 可供使用。</span><span class="sxs-lookup"><span data-stu-id="a743e-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="a743e-142">然後，使用者可以手動重新開機其系統，或在兩個小時之後，自動重新開機裝置以完成升級。</span><span class="sxs-lookup"><span data-stu-id="a743e-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="a743e-143">使用者會在自動重新開機前10分鐘收到提醒通知。</span><span class="sxs-lookup"><span data-stu-id="a743e-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="a743e-144">裝置重新啟動之後，版本升級程序便完成。</span><span class="sxs-lookup"><span data-stu-id="a743e-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="a743e-145">使用者將會收到成功升級的通知。</span><span class="sxs-lookup"><span data-stu-id="a743e-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="a743e-146">如果另一個原則需要在執行 <strong>changepk.exe</strong> 時發生系統重新開機，則版本升級將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a743e-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="a743e-147">如果在佈建套件中輸入產品金鑰，而且使用者開始安裝套件，會向使用者顯示通知，告知他們的系統會重新啟動才能完成套件安裝。</span><span class="sxs-lookup"><span data-stu-id="a743e-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="a743e-148">明確同意使用者進行時，套件會繼續安裝，並使用產品金鑰 <strong>changepk.exe</strong> 執行。</span><span class="sxs-lookup"><span data-stu-id="a743e-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="a743e-149">自動重新開機之前使用者將會收到提醒通知 30 秒。</span><span class="sxs-lookup"><span data-stu-id="a743e-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="a743e-150">裝置重新啟動之後，版本升級程序便完成。</span><span class="sxs-lookup"><span data-stu-id="a743e-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="a743e-151">使用者將會收到成功升級的通知。</span><span class="sxs-lookup"><span data-stu-id="a743e-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="a743e-152">此節點也可用來在特定版本的 Windows 10 桌面裝置上，藉由輸入產品金鑰來啟用或變更產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="a743e-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="a743e-153">啟用或變更產品金鑰不需要重新開機，而且是使用者的無訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="a743e-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="a743e-154">輸入的產品金鑰必須是29個字元 (也就是說，它應該包含連字號) ，否則 Windows 10 桌面裝置上的啟用、版本升級或產品金鑰變更將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a743e-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="a743e-155">從 Microsoft 大量授權服務中心取得產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="a743e-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="a743e-156">您的組織必須具有 Microsoft 的大量授權合約，才能存取入口網站。</span><span class="sxs-lookup"><span data-stu-id="a743e-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="a743e-157">以下是透過 MDM 使用此節點時的有效版本升級路徑：</span><span class="sxs-lookup"><span data-stu-id="a743e-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="a743e-158">Windows 10 企業版至 Windows 10 教育版</span><span class="sxs-lookup"><span data-stu-id="a743e-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="a743e-159">Windows 10 家用版至 Windows 10 教育版</span><span class="sxs-lookup"><span data-stu-id="a743e-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="a743e-160">Windows 10 專業版至 Windows 10 教育版</span><span class="sxs-lookup"><span data-stu-id="a743e-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="a743e-161">Windows 10 專業版至 Windows 10 企業版</span><span class="sxs-lookup"><span data-stu-id="a743e-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="a743e-162">您可以在下列版本上執行啟用或變更產品金鑰：</span><span class="sxs-lookup"><span data-stu-id="a743e-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="a743e-163">Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="a743e-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="a743e-164">Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="a743e-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="a743e-165">Windows 10 Home</span><span class="sxs-lookup"><span data-stu-id="a743e-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="a743e-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="a743e-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="a743e-167">屬性</span><span class="sxs-lookup"><span data-stu-id="a743e-167">Properties</span></span>

<span data-ttu-id="a743e-168">**MDM \_ WindowsLicensing** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a743e-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a743e-169">版本(Edition)</span><span class="sxs-lookup"><span data-stu-id="a743e-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a743e-170">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a743e-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a743e-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a743e-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a743e-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a743e-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a743e-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a743e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a743e-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a743e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a743e-175">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a743e-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a743e-176">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a743e-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="a743e-177">LicenseKeyType</span><span class="sxs-lookup"><span data-stu-id="a743e-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a743e-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a743e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a743e-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a743e-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a743e-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a743e-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a743e-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a743e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a743e-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a743e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a743e-183">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a743e-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a743e-184">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a743e-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="a743e-185">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="a743e-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="a743e-186">狀態</span><span class="sxs-lookup"><span data-stu-id="a743e-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a743e-187">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a743e-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a743e-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a743e-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a743e-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="a743e-189">Requirements</span></span>



| <span data-ttu-id="a743e-190">需求</span><span class="sxs-lookup"><span data-stu-id="a743e-190">Requirement</span></span> | <span data-ttu-id="a743e-191">值</span><span class="sxs-lookup"><span data-stu-id="a743e-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a743e-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a743e-192">Minimum supported client</span></span><br/> | <span data-ttu-id="a743e-193">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a743e-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a743e-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a743e-194">Minimum supported server</span></span><br/> | <span data-ttu-id="a743e-195">都不支援</span><span class="sxs-lookup"><span data-stu-id="a743e-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a743e-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="a743e-196">Namespace</span></span><br/>                | <span data-ttu-id="a743e-197">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="a743e-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a743e-198">MOF</span><span class="sxs-lookup"><span data-stu-id="a743e-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a743e-199"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a743e-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a743e-200">DLL</span><span class="sxs-lookup"><span data-stu-id="a743e-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a743e-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a743e-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a743e-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a743e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a743e-203">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a743e-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

