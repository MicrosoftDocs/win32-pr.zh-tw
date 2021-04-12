---
title: MDM_Policy_Config01_CredentialProviders02 類別
description: MDM \_ Policy \_ Config01 CredentialProviders02 類別會設定 \_ 可用的認證提供者原則。
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- MDM_Policy_Config01_CredentialProviders02 類別
- MDM_Policy_Config01_CredentialProviders02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464848"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="e59fc-105">MDM \_ 原則 \_ Config01 \_ CredentialProviders02 類別</span><span class="sxs-lookup"><span data-stu-id="e59fc-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="e59fc-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e59fc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e59fc-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e59fc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e59fc-108">MDM \_ Policy \_ Config01 CredentialProviders02 類別會設定 \_ 可用的認證提供者原則。</span><span class="sxs-lookup"><span data-stu-id="e59fc-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="e59fc-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e59fc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59fc-110">語法</span><span class="sxs-lookup"><span data-stu-id="e59fc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="e59fc-111">成員</span><span class="sxs-lookup"><span data-stu-id="e59fc-111">Members</span></span>

<span data-ttu-id="e59fc-112">**MDM \_ Policy \_ Config01 \_ CredentialProviders02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e59fc-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="e59fc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e59fc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e59fc-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e59fc-114">Properties</span></span>

<span data-ttu-id="e59fc-115">**MDM \_ Policy \_ Config01 \_ CredentialProviders02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e59fc-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e59fc-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="e59fc-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59fc-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e59fc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e59fc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e59fc-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="e59fc-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59fc-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e59fc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e59fc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e59fc-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="e59fc-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59fc-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e59fc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e59fc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e59fc-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e59fc-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59fc-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e59fc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e59fc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e59fc-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e59fc-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e59fc-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e59fc-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e59fc-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e59fc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e59fc-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e59fc-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e59fc-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e59fc-133">Requirements</span></span>



| <span data-ttu-id="e59fc-134">需求</span><span class="sxs-lookup"><span data-stu-id="e59fc-134">Requirement</span></span> | <span data-ttu-id="e59fc-135">值</span><span class="sxs-lookup"><span data-stu-id="e59fc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e59fc-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e59fc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e59fc-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e59fc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e59fc-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e59fc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e59fc-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="e59fc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e59fc-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="e59fc-140">Namespace</span></span><br/>                | <span data-ttu-id="e59fc-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e59fc-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e59fc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e59fc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e59fc-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e59fc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e59fc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e59fc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e59fc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e59fc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

