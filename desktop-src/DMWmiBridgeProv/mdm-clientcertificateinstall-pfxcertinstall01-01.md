---
title: MDM_ClientCertificateInstall_PFXCertInstall01_01 類別
description: MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01 類別可讓企業使用唯一識別碼來區分不同的憑證安裝要求。
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- MDM_ClientCertificateInstall_PFXCertInstall01_01 類別
- MDM_ClientCertificateInstall_PFXCertInstall01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105017"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="e35c4-105">MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="e35c4-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="e35c4-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e35c4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e35c4-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e35c4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e35c4-108">**MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** 類別可讓企業使用唯一識別碼來區分不同的憑證安裝要求。</span><span class="sxs-lookup"><span data-stu-id="e35c4-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="e35c4-109">需要安裝 PFX 憑證。</span><span class="sxs-lookup"><span data-stu-id="e35c4-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="e35c4-110">在此節點上呼叫 Delete，應刪除對應的 PFX blob 所安裝的憑證和金鑰。</span><span class="sxs-lookup"><span data-stu-id="e35c4-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="e35c4-111">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e35c4-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e35c4-112">語法</span><span class="sxs-lookup"><span data-stu-id="e35c4-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="e35c4-113">成員</span><span class="sxs-lookup"><span data-stu-id="e35c4-113">Members</span></span>

<span data-ttu-id="e35c4-114">**MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e35c4-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e35c4-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e35c4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e35c4-116">屬性</span><span class="sxs-lookup"><span data-stu-id="e35c4-116">Properties</span></span>

<span data-ttu-id="e35c4-117">**MDM \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e35c4-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e35c4-118">容器</span><span class="sxs-lookup"><span data-stu-id="e35c4-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e35c4-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e35c4-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e35c4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e35c4-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e35c4-125">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e35c4-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="e35c4-126">針對此類別，這是用來區分不同憑證安裝要求的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e35c4-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="e35c4-127">KeyLocation</span><span class="sxs-lookup"><span data-stu-id="e35c4-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e35c4-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e35c4-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e35c4-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e35c4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e35c4-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e35c4-134">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e35c4-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="e35c4-135">字串為 "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span><span class="sxs-lookup"><span data-stu-id="e35c4-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="e35c4-136">PFXCertBlob</span><span class="sxs-lookup"><span data-stu-id="e35c4-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-139">限定詞： **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="e35c4-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-140">PFXCertPassword</span><span class="sxs-lookup"><span data-stu-id="e35c4-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-143">PFXCertPasswordEncryptionStore</span><span class="sxs-lookup"><span data-stu-id="e35c4-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-146">PFXCertPasswordEncryptionType</span><span class="sxs-lookup"><span data-stu-id="e35c4-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e35c4-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-149">PFXKeyExportable</span><span class="sxs-lookup"><span data-stu-id="e35c4-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e35c4-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-152">狀態</span><span class="sxs-lookup"><span data-stu-id="e35c4-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e35c4-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e35c4-155">指紋</span><span class="sxs-lookup"><span data-stu-id="e35c4-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e35c4-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e35c4-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e35c4-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e35c4-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e35c4-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="e35c4-158">Requirements</span></span>



| <span data-ttu-id="e35c4-159">需求</span><span class="sxs-lookup"><span data-stu-id="e35c4-159">Requirement</span></span> | <span data-ttu-id="e35c4-160">值</span><span class="sxs-lookup"><span data-stu-id="e35c4-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e35c4-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e35c4-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e35c4-162">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e35c4-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e35c4-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e35c4-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e35c4-164">都不支援</span><span class="sxs-lookup"><span data-stu-id="e35c4-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e35c4-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="e35c4-165">Namespace</span></span><br/>                | <span data-ttu-id="e35c4-166">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e35c4-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e35c4-167">MOF</span><span class="sxs-lookup"><span data-stu-id="e35c4-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e35c4-168"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e35c4-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e35c4-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e35c4-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e35c4-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e35c4-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e35c4-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e35c4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e35c4-172">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="e35c4-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

