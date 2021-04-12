---
title: MDM_ClientCertificateInstall_Install03 類別
description: MDM \_ ClientCertificateInstall \_ Install03 類別可讓企業設定用戶端憑證的安裝。
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- MDM_ClientCertificateInstall_Install03 類別
- MDM_ClientCertificateInstall_Install03 類別，描述
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105018"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="a23e1-105">MDM \_ ClientCertificateInstall \_ Install03 類別</span><span class="sxs-lookup"><span data-stu-id="a23e1-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="a23e1-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a23e1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a23e1-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a23e1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a23e1-108">**MDM \_ ClientCertificateInstall \_ Install03** 類別可讓企業設定用戶端憑證的安裝。SCEP 憑證註冊的必要參數。</span><span class="sxs-lookup"><span data-stu-id="a23e1-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="a23e1-109">用來將 SCEP cert 安裝相關要求分組的父節點。</span><span class="sxs-lookup"><span data-stu-id="a23e1-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="a23e1-110">雖然 [安裝支援] 下的子節點會取代命令，但是在將 Exec 命令傳送至裝置之後，裝置將會採用接受 Exec 命令時所設定的值。</span><span class="sxs-lookup"><span data-stu-id="a23e1-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="a23e1-111">在接受 Exec 命令之後，伺服器應該不會預期節點值變更，將會影響目前正在進行的註冊。</span><span class="sxs-lookup"><span data-stu-id="a23e1-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="a23e1-112">在變更子節點值之前，伺服器應該檢查狀態節點的值，並確定裝置不是處於未知的階段。</span><span class="sxs-lookup"><span data-stu-id="a23e1-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="a23e1-113">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a23e1-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23e1-114">語法</span><span class="sxs-lookup"><span data-stu-id="a23e1-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="a23e1-115">成員</span><span class="sxs-lookup"><span data-stu-id="a23e1-115">Members</span></span>

<span data-ttu-id="a23e1-116">**MDM \_ ClientCertificateInstall \_ Install03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a23e1-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="a23e1-117">方法</span><span class="sxs-lookup"><span data-stu-id="a23e1-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="a23e1-118">屬性</span><span class="sxs-lookup"><span data-stu-id="a23e1-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a23e1-119">方法</span><span class="sxs-lookup"><span data-stu-id="a23e1-119">Methods</span></span>

<span data-ttu-id="a23e1-120">**MDM \_ ClientCertificateInstall \_ Install03** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a23e1-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="a23e1-121">方法</span><span class="sxs-lookup"><span data-stu-id="a23e1-121">Method</span></span>                                                                      | <span data-ttu-id="a23e1-122">描述</span><span class="sxs-lookup"><span data-stu-id="a23e1-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="a23e1-123">**EnrollMethod**</span><span class="sxs-lookup"><span data-stu-id="a23e1-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="a23e1-124">必要。</span><span class="sxs-lookup"><span data-stu-id="a23e1-124">Required.</span></span> <span data-ttu-id="a23e1-125">觸發裝置以啟動憑證註冊。</span><span class="sxs-lookup"><span data-stu-id="a23e1-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a23e1-126">屬性</span><span class="sxs-lookup"><span data-stu-id="a23e1-126">Properties</span></span>

<span data-ttu-id="a23e1-127">**MDM \_ ClientCertificateInstall \_ Install03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a23e1-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a23e1-128">AADKeyIdentifierList</span><span class="sxs-lookup"><span data-stu-id="a23e1-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-131">CAThumbprint</span><span class="sxs-lookup"><span data-stu-id="a23e1-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-134">挑戰</span><span class="sxs-lookup"><span data-stu-id="a23e1-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-137">容器</span><span class="sxs-lookup"><span data-stu-id="a23e1-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-140">CustomTextToShowInPrompt</span><span class="sxs-lookup"><span data-stu-id="a23e1-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-143">EKUMapping</span><span class="sxs-lookup"><span data-stu-id="a23e1-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a23e1-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a23e1-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a23e1-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a23e1-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a23e1-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a23e1-153">SCEP 憑證註冊的必要參數。</span><span class="sxs-lookup"><span data-stu-id="a23e1-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="a23e1-154">用來將 SCEP cert 安裝相關要求分組的父節點。</span><span class="sxs-lookup"><span data-stu-id="a23e1-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="a23e1-155">格式為 node。</span><span class="sxs-lookup"><span data-stu-id="a23e1-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="a23e1-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="a23e1-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-157">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-159">KeyProtection</span><span class="sxs-lookup"><span data-stu-id="a23e1-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-160">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-162">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="a23e1-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-163">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a23e1-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a23e1-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a23e1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-168">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a23e1-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a23e1-169">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a23e1-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="a23e1-170">字串為 "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span><span class="sxs-lookup"><span data-stu-id="a23e1-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="a23e1-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="a23e1-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-172">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-174">RetryDelay</span><span class="sxs-lookup"><span data-stu-id="a23e1-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-175">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="a23e1-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-180">SubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="a23e1-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="a23e1-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="a23e1-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-189">ValidPeriod</span><span class="sxs-lookup"><span data-stu-id="a23e1-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a23e1-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a23e1-192">ValidPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="a23e1-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a23e1-193">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a23e1-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a23e1-194">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a23e1-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a23e1-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="a23e1-195">Requirements</span></span>



| <span data-ttu-id="a23e1-196">需求</span><span class="sxs-lookup"><span data-stu-id="a23e1-196">Requirement</span></span> | <span data-ttu-id="a23e1-197">值</span><span class="sxs-lookup"><span data-stu-id="a23e1-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a23e1-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a23e1-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a23e1-199">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a23e1-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a23e1-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a23e1-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a23e1-201">都不支援</span><span class="sxs-lookup"><span data-stu-id="a23e1-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a23e1-202">命名空間</span><span class="sxs-lookup"><span data-stu-id="a23e1-202">Namespace</span></span><br/>                | <span data-ttu-id="a23e1-203">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a23e1-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a23e1-204">MOF</span><span class="sxs-lookup"><span data-stu-id="a23e1-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a23e1-205"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a23e1-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a23e1-206">DLL</span><span class="sxs-lookup"><span data-stu-id="a23e1-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a23e1-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a23e1-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a23e1-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a23e1-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23e1-209">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a23e1-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

