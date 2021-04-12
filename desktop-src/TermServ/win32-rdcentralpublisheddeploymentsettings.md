---
title: Win32_RDCentralPublishedDeploymentSettings 類別
description: 包含用來為從伺服器陣列發佈的資源產生 RDP 檔案的部署設定。
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedDeploymentSettings 類別遠端桌面服務
- Win32_RDCentralPublishedDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385162"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="8e7cb-105">Win32 \_ RDCentralPublishedDeploymentSettings 類別</span><span class="sxs-lookup"><span data-stu-id="8e7cb-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="8e7cb-106">包含用來為從伺服器陣列發佈的資源產生 RDP 檔案的部署設定。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="8e7cb-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7cb-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e7cb-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="8e7cb-109">成員</span><span class="sxs-lookup"><span data-stu-id="8e7cb-109">Members</span></span>

<span data-ttu-id="8e7cb-110">**Win32 \_ RDCentralPublishedDeploymentSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e7cb-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="8e7cb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8e7cb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e7cb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8e7cb-112">Properties</span></span>

<span data-ttu-id="8e7cb-113">**Win32 \_ RDCentralPublishedDeploymentSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e7cb-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-115">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-117">**true** 表示允許字型平滑;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7cb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-122">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8e7cb-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-125">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="8e7cb-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-127">用來簽署 RDP 檔案的憑證;只有當 *HasCertificate* 為 true 時，才必須如此。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-128">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-131">包含色彩位深度：</span><span class="sxs-lookup"><span data-stu-id="8e7cb-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="8e7cb-132">**4** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="8e7cb-133">**8** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="8e7cb-134">**15** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="8e7cb-135">**16** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="8e7cb-136">**24** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="8e7cb-137">**32** () </span><span class="sxs-lookup"><span data-stu-id="8e7cb-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7cb-138">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-141">包含對應至自訂 RDP 設定的 RDP 檔案內容。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-142">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-145">包含對應至部署設定之 RDP 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="8e7cb-146">如果設定此參數，系統將會使用這個 RDP 檔案，並忽略此呼叫中的其他 RDP 設定。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-147">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7cb-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-150">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-150">Description of the object.</span></span>

<span data-ttu-id="8e7cb-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-152">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-155">伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-156">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-157">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-159">包含閘道驗證模式：</span><span class="sxs-lookup"><span data-stu-id="8e7cb-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="8e7cb-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**密碼 (0)** (0) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="8e7cb-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**智慧卡 (1)** (1) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="8e7cb-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**允許使用者選擇 (4)** (4) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7cb-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-166">閘道器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-167">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-170">說明如何使用閘道：</span><span class="sxs-lookup"><span data-stu-id="8e7cb-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="8e7cb-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8e7cb-172">沒有閘道。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="8e7cb-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8e7cb-174">使用本機閘道傳遞。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="8e7cb-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8e7cb-176">使用閘道。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="8e7cb-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e7cb-178">偵測閘道。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7cb-179">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-182">**true** 表示盡可能使用 ts 閘道和 ts 伺服器的相同使用者認證;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-183">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-186">**true** 表示使用憑證來簽署 RDP 檔案;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-188">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7cb-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-190">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="8e7cb-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-191">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-191">The date the object was installed.</span></span> <span data-ttu-id="8e7cb-192">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8e7cb-193">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-194">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7cb-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-197">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-197">The name of the object.</span></span>

<span data-ttu-id="8e7cb-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-199">**通訊埠**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-200">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-202">RDP 埠。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-203">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-206">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e7cb-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-207">發佈應用程式之伺服器陣列的別名。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-208">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-209">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-210">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-211">重新導向選項：</span><span class="sxs-lookup"><span data-stu-id="8e7cb-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="8e7cb-212">0</span><span class="sxs-lookup"><span data-stu-id="8e7cb-212">0</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-213">無</span><span class="sxs-lookup"><span data-stu-id="8e7cb-213">None</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-214">1</span><span class="sxs-lookup"><span data-stu-id="8e7cb-214">1</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-215">磁碟機</span><span class="sxs-lookup"><span data-stu-id="8e7cb-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-216">2</span><span class="sxs-lookup"><span data-stu-id="8e7cb-216">2</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-217">印表機</span><span class="sxs-lookup"><span data-stu-id="8e7cb-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-218">4</span><span class="sxs-lookup"><span data-stu-id="8e7cb-218">4</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-219">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="8e7cb-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-220">8</span><span class="sxs-lookup"><span data-stu-id="8e7cb-220">8</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-221">隨插即用</span><span class="sxs-lookup"><span data-stu-id="8e7cb-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="8e7cb-222">16</span><span class="sxs-lookup"><span data-stu-id="8e7cb-222">16</span></span>
</dt> <dd>

<span data-ttu-id="8e7cb-223">智慧卡</span><span class="sxs-lookup"><span data-stu-id="8e7cb-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7cb-224">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e7cb-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-227">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-228">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-228">Current status of the object.</span></span> <span data-ttu-id="8e7cb-229">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8e7cb-230">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8e7cb-231">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e7cb-232">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e7cb-233">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e7cb-234">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8e7cb-235"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-236"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-237"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-238"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-239"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-240"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-241"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7cb-242"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="8e7cb-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e7cb-243">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7cb-244">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e7cb-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e7cb-245">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e7cb-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8e7cb-246">**true** 表示啟用桌面的多重監視器 (不使用滑軌) ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="8e7cb-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e7cb-247">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e7cb-247">Requirements</span></span>



| <span data-ttu-id="8e7cb-248">需求</span><span class="sxs-lookup"><span data-stu-id="8e7cb-248">Requirement</span></span> | <span data-ttu-id="8e7cb-249">值</span><span class="sxs-lookup"><span data-stu-id="8e7cb-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7cb-250">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e7cb-250">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7cb-251">都不支援</span><span class="sxs-lookup"><span data-stu-id="8e7cb-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8e7cb-252">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e7cb-252">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7cb-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e7cb-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="8e7cb-254">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e7cb-254">Namespace</span></span><br/>                | <span data-ttu-id="8e7cb-255">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8e7cb-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8e7cb-256">MOF</span><span class="sxs-lookup"><span data-stu-id="8e7cb-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e7cb-257"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e7cb-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="8e7cb-258">DLL</span><span class="sxs-lookup"><span data-stu-id="8e7cb-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e7cb-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e7cb-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

