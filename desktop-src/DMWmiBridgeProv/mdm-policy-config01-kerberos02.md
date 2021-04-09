---
title: MDM_Policy_Config01_Kerberos02 類別
description: MDM \_ Policy \_ Config01 Kerberos02 類別會設定 \_ Kerberos 原則。
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- MDM_Policy_Config01_Kerberos02 類別
- MDM_Policy_Config01_Kerberos02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843555"
---
# <a name="mdm_policy_config01_kerberos02-class"></a><span data-ttu-id="ea212-105">MDM \_ 原則 \_ Config01 \_ Kerberos02 類別</span><span class="sxs-lookup"><span data-stu-id="ea212-105">MDM\_Policy\_Config01\_Kerberos02 class</span></span>

<span data-ttu-id="ea212-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ea212-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ea212-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ea212-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ea212-108">MDM \_ Policy \_ Config01 Kerberos02 類別會設定 \_ Kerberos 原則。</span><span class="sxs-lookup"><span data-stu-id="ea212-108">The MDM\_Policy\_Config01\_Kerberos02 class configures the Kerberos policies.</span></span>

<span data-ttu-id="ea212-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea212-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea212-110">語法</span><span class="sxs-lookup"><span data-stu-id="ea212-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="ea212-111">成員</span><span class="sxs-lookup"><span data-stu-id="ea212-111">Members</span></span>

<span data-ttu-id="ea212-112">**MDM \_ Policy \_ Config01 \_ Kerberos02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea212-112">The **MDM\_Policy\_Config01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="ea212-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ea212-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea212-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ea212-114">Properties</span></span>

<span data-ttu-id="ea212-115">**MDM \_ Policy \_ Config01 \_ Kerberos02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ea212-115">The **MDM\_Policy\_Config01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ea212-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="ea212-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea212-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea212-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ea212-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea212-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea212-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ea212-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ea212-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="ea212-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea212-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea212-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ea212-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea212-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea212-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ea212-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ea212-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="ea212-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea212-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ea212-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="ea212-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea212-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ea212-136">SetMaximumCoNtextTokenSize</span><span class="sxs-lookup"><span data-stu-id="ea212-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea212-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea212-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea212-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea212-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea212-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea212-139">Requirements</span></span>



| <span data-ttu-id="ea212-140">需求</span><span class="sxs-lookup"><span data-stu-id="ea212-140">Requirement</span></span> | <span data-ttu-id="ea212-141">值</span><span class="sxs-lookup"><span data-stu-id="ea212-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea212-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea212-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ea212-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea212-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea212-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea212-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ea212-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="ea212-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ea212-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="ea212-146">Namespace</span></span><br/>                | <span data-ttu-id="ea212-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ea212-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ea212-148">MOF</span><span class="sxs-lookup"><span data-stu-id="ea212-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea212-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea212-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea212-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ea212-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea212-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea212-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

