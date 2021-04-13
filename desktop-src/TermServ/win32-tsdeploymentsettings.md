---
title: Win32_TSDeploymentSettings 類別
description: 定義 RemoteApp 管理員在建立遠端桌面通訊協定 (RDP) 檔案時所使用的預設設定。
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings 類別遠端桌面服務
- Win32_TSDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465092"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="5ab77-105">Win32 \_ TSDeploymentSettings 類別</span><span class="sxs-lookup"><span data-stu-id="5ab77-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="5ab77-106">定義 RemoteApp 管理員在建立遠端桌面通訊協定 (RDP) 檔案時所使用的預設設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="5ab77-107">這些設定不會影響任何已發佈的應用程式或桌上型電腦。</span><span class="sxs-lookup"><span data-stu-id="5ab77-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab77-108">語法</span><span class="sxs-lookup"><span data-stu-id="5ab77-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="5ab77-109">成員</span><span class="sxs-lookup"><span data-stu-id="5ab77-109">Members</span></span>

<span data-ttu-id="5ab77-110">**Win32 \_ TSDeploymentSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5ab77-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5ab77-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5ab77-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ab77-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5ab77-112">Properties</span></span>

<span data-ttu-id="5ab77-113">**Win32 \_ TSDeploymentSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5ab77-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ab77-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="5ab77-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-115">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab77-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-117">指出是否允許字型平滑。</span><span class="sxs-lookup"><span data-stu-id="5ab77-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="5ab77-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab77-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5ab77-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-122">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="5ab77-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5ab77-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-124">**CertificateExpiresOn**</span><span class="sxs-lookup"><span data-stu-id="5ab77-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-127">憑證到期的日期。</span><span class="sxs-lookup"><span data-stu-id="5ab77-127">The date that the certificate expires on.</span></span> <span data-ttu-id="5ab77-128">此值會儲存為64位 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 格式。</span><span class="sxs-lookup"><span data-stu-id="5ab77-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="5ab77-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-130">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="5ab77-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-132">用來簽署 RDP 檔案的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="5ab77-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-133">**CertificateIssuedBy**</span><span class="sxs-lookup"><span data-stu-id="5ab77-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-136">指定憑證的簽發者。</span><span class="sxs-lookup"><span data-stu-id="5ab77-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-137">**CertificateIssuedTo**</span><span class="sxs-lookup"><span data-stu-id="5ab77-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-140">指定憑證的發行物件。</span><span class="sxs-lookup"><span data-stu-id="5ab77-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-141">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="5ab77-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-142">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ab77-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-144">顯示器的色彩位深度。</span><span class="sxs-lookup"><span data-stu-id="5ab77-144">The color bit depth of the display.</span></span> <span data-ttu-id="5ab77-145">可能的值為4、8、15、16、24和32。</span><span class="sxs-lookup"><span data-stu-id="5ab77-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-146">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="5ab77-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-149">RDP 檔案的內容，對應至 RemoteApp 管理員中的自訂 RDP 設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-150">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="5ab77-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-153">RDP 檔案的內容，對應至 RemoteApp 管理員中的部署設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="5ab77-154">如果設定此值，RDP 部署設定會取代此類別中的預設設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="5ab77-155">例如，如果您在這個類別中設定 **GatewayAuthMode** 屬性，並設定 **DeploymentRDPSettings** 屬性，則會忽略這個類別的 **GatewayAuthMode** 屬性，並使用 **DeploymentRDPSettings** 的 **GatewayAuthMode** 值。</span><span class="sxs-lookup"><span data-stu-id="5ab77-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-156">**說明**</span><span class="sxs-lookup"><span data-stu-id="5ab77-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab77-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-159">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5ab77-159">Description of the object.</span></span>

<span data-ttu-id="5ab77-160">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-161">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="5ab77-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-164">RD 工作階段主機伺服器的名稱，或 RD 工作階段主機伺服器陣列 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab77-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-165">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="5ab77-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-166">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ab77-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-168">RD 閘道的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="5ab77-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="5ab77-169">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="5ab77-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5ab77-170">0</span><span class="sxs-lookup"><span data-stu-id="5ab77-170">0</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-171">密碼</span><span class="sxs-lookup"><span data-stu-id="5ab77-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-172">1</span><span class="sxs-lookup"><span data-stu-id="5ab77-172">1</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-173">智慧卡</span><span class="sxs-lookup"><span data-stu-id="5ab77-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-174">4</span><span class="sxs-lookup"><span data-stu-id="5ab77-174">4</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-175">允許使用者在連接期間進行選取。</span><span class="sxs-lookup"><span data-stu-id="5ab77-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab77-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="5ab77-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-179">要使用 RD 閘道伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab77-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-180">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="5ab77-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-181">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ab77-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-183">指出是否要使用 RD 閘道伺服器來連接到整個防火牆的目標 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="5ab77-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="5ab77-184">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="5ab77-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5ab77-185">0</span><span class="sxs-lookup"><span data-stu-id="5ab77-185">0</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-186">請勿使用 RD 閘道的伺服器。</span><span class="sxs-lookup"><span data-stu-id="5ab77-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-187">1</span><span class="sxs-lookup"><span data-stu-id="5ab77-187">1</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-188">使用 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="5ab77-188">Use an RD Gateway server.</span></span> <span data-ttu-id="5ab77-189">略過本機位址的 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="5ab77-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-190">2</span><span class="sxs-lookup"><span data-stu-id="5ab77-190">2</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-191">使用 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="5ab77-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-192">3</span><span class="sxs-lookup"><span data-stu-id="5ab77-192">3</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-193">自動偵測 RD 閘道伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab77-194">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="5ab77-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-195">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab77-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-197">可能的話，請針對 RD 閘道伺服器和 RD 工作階段主機伺服器使用相同的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="5ab77-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-198">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="5ab77-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-199">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab77-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-200">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-201">指出是否要使用憑證來簽署 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="5ab77-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ab77-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-203">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5ab77-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab77-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-205">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="5ab77-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-206">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="5ab77-206">The date the object was installed.</span></span> <span data-ttu-id="5ab77-207">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="5ab77-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5ab77-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-209">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5ab77-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab77-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-212">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab77-212">The name of the object.</span></span>

<span data-ttu-id="5ab77-213">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-214">**通訊埠**</span><span class="sxs-lookup"><span data-stu-id="5ab77-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-215">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ab77-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-217">要使用的 RDP 埠。</span><span class="sxs-lookup"><span data-stu-id="5ab77-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-218">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="5ab77-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-219">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ab77-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-221">指定 RemoteApp 連接的裝置和資源重新導向選項。</span><span class="sxs-lookup"><span data-stu-id="5ab77-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="5ab77-222">可以結合 **RedirectionOptions** 的旗標。</span><span class="sxs-lookup"><span data-stu-id="5ab77-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="5ab77-223">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="5ab77-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="5ab77-224">0</span><span class="sxs-lookup"><span data-stu-id="5ab77-224">0</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-225">無裝置或資源重新導向。</span><span class="sxs-lookup"><span data-stu-id="5ab77-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-226">1</span><span class="sxs-lookup"><span data-stu-id="5ab77-226">1</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-227">重新導向磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5ab77-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-228">2</span><span class="sxs-lookup"><span data-stu-id="5ab77-228">2</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-229">重新導向印表機。</span><span class="sxs-lookup"><span data-stu-id="5ab77-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-230">4</span><span class="sxs-lookup"><span data-stu-id="5ab77-230">4</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-231">重新導向剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="5ab77-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-232">8</span><span class="sxs-lookup"><span data-stu-id="5ab77-232">8</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-233">重新導向支援的隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="5ab77-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-234">16</span><span class="sxs-lookup"><span data-stu-id="5ab77-234">16</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-235">重新導向智慧卡。</span><span class="sxs-lookup"><span data-stu-id="5ab77-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-236">32</span><span class="sxs-lookup"><span data-stu-id="5ab77-236">32</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-237">重新導向音訊。</span><span class="sxs-lookup"><span data-stu-id="5ab77-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-238">64</span><span class="sxs-lookup"><span data-stu-id="5ab77-238">64</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-239">重新導向序列埠。</span><span class="sxs-lookup"><span data-stu-id="5ab77-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab77-240">**RequireServerAuth**</span><span class="sxs-lookup"><span data-stu-id="5ab77-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-241">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab77-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-242">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-243">指出是否需要伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="5ab77-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5ab77-244">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5ab77-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab77-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab77-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-247">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="5ab77-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-248">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5ab77-248">Current status of the object.</span></span> <span data-ttu-id="5ab77-249">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="5ab77-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5ab77-250">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="5ab77-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5ab77-251">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5ab77-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ab77-252">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="5ab77-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ab77-253">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5ab77-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ab77-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5ab77-255"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-256"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-257"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-258"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-259"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-260"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-261"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab77-262"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="5ab77-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab77-263">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="5ab77-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab77-264">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab77-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab77-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab77-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ab77-266">指出是否已啟用桌面的多個監視器。</span><span class="sxs-lookup"><span data-stu-id="5ab77-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ab77-267">備註</span><span class="sxs-lookup"><span data-stu-id="5ab77-267">Remarks</span></span>

<span data-ttu-id="5ab77-268">您必須是 Administrators 群組的成員，才能使用這個類別來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5ab77-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="5ab77-269">如果 **RequireServerAuth** 設定為 **TRUE**，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="5ab77-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="5ab77-270">如果 RemoteApp 程式適用于內部網路，而且所有用戶端電腦都是執行 Windows Server 2008 或 Windows Vista，您就不需要設定 RD 工作階段主機伺服器來使用 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="5ab77-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="5ab77-271">在此案例中，是使用網路層級驗證。</span><span class="sxs-lookup"><span data-stu-id="5ab77-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="5ab77-272">您必須為 **FarmName** 屬性的值指定伺服器或伺服器陣列的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5ab77-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="5ab77-273">若要連接到 "CIMV2 \\ microsoft-windows-terminalservices-gateway" 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="5ab77-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5ab77-274">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="5ab77-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="5ab77-275">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="5ab77-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5ab77-276">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="5ab77-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5ab77-277">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5ab77-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ab77-278">當您新增相關聯的角色時，它們會安裝在電腦上。</span><span class="sxs-lookup"><span data-stu-id="5ab77-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="5ab77-279">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5ab77-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab77-280">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ab77-280">Requirements</span></span>



| <span data-ttu-id="5ab77-281">需求</span><span class="sxs-lookup"><span data-stu-id="5ab77-281">Requirement</span></span> | <span data-ttu-id="5ab77-282">值</span><span class="sxs-lookup"><span data-stu-id="5ab77-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab77-283">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ab77-283">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab77-284">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ab77-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5ab77-285">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ab77-285">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab77-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ab77-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ab77-287">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ab77-287">Namespace</span></span><br/>                | <span data-ttu-id="5ab77-288">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5ab77-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5ab77-289">MOF</span><span class="sxs-lookup"><span data-stu-id="5ab77-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ab77-290"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5ab77-291">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab77-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab77-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

