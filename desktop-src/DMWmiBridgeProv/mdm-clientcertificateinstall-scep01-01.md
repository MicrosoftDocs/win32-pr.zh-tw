---
title: MDM_ClientCertificateInstall_SCEP01_01 類別
description: MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01 類別可讓您存取 SCEP 憑證安裝的節點，並使用唯一識別碼來區分不同的憑證安裝要求。
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- MDM_ClientCertificateInstall_SCEP01_01 類別
- MDM_ClientCertificateInstall_SCEP01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843975"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="fd6f8-105">MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="fd6f8-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="fd6f8-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd6f8-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fd6f8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd6f8-108">**MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** 類別可讓您存取 SCEP 憑證安裝的節點，並使用唯一識別碼來區分不同的憑證安裝要求。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="fd6f8-109">需要安裝 SCEP 憑證。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="fd6f8-110">支援的作業為 Get、Add 和 Delete。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="fd6f8-111">在此節點上呼叫 Delete 應該會刪除對應的 SCEP 憑證。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="fd6f8-112">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6f8-113">語法</span><span class="sxs-lookup"><span data-stu-id="fd6f8-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="fd6f8-114">成員</span><span class="sxs-lookup"><span data-stu-id="fd6f8-114">Members</span></span>

<span data-ttu-id="fd6f8-115">**MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd6f8-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fd6f8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="fd6f8-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd6f8-117">屬性</span><span class="sxs-lookup"><span data-stu-id="fd6f8-117">Properties</span></span>

<span data-ttu-id="fd6f8-118">**MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd6f8-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd6f8-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd6f8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd6f8-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="fd6f8-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd6f8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd6f8-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd6f8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd6f8-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd6f8-129">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="fd6f8-130">針對此類別，這是用來區分不同憑證安裝要求的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f8-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd6f8-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd6f8-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd6f8-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fd6f8-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="fd6f8-136">字串為 "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span><span class="sxs-lookup"><span data-stu-id="fd6f8-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="fd6f8-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="fd6f8-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd6f8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fd6f8-140">狀態</span><span class="sxs-lookup"><span data-stu-id="fd6f8-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f8-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd6f8-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f8-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd6f8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd6f8-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd6f8-143">Requirements</span></span>



| <span data-ttu-id="fd6f8-144">需求</span><span class="sxs-lookup"><span data-stu-id="fd6f8-144">Requirement</span></span> | <span data-ttu-id="fd6f8-145">值</span><span class="sxs-lookup"><span data-stu-id="fd6f8-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6f8-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd6f8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6f8-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd6f8-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd6f8-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd6f8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6f8-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd6f8-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fd6f8-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd6f8-150">Namespace</span></span><br/>                | <span data-ttu-id="fd6f8-151">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fd6f8-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fd6f8-152">MOF</span><span class="sxs-lookup"><span data-stu-id="fd6f8-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd6f8-153"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd6f8-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd6f8-154">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6f8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6f8-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6f8-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6f8-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd6f8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6f8-157">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="fd6f8-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

