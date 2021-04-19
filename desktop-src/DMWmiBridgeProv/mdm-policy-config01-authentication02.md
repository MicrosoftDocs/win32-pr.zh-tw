---
title: MDM_Policy_Config01_Authentication02 類別
description: MDM \_ Policy \_ Config01 \_ Authentication02 類別代表可用的驗證管理原則。
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- MDM_Policy_Config01_Authentication02 類別
- MDM_Policy_Config01_Authentication02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967531"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="6f0b0-105">MDM \_ 原則 \_ Config01 \_ Authentication02 類別</span><span class="sxs-lookup"><span data-stu-id="6f0b0-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="6f0b0-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f0b0-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6f0b0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6f0b0-108">**MDM \_ Policy \_ Config01 \_ Authentication02** 類別代表可用的驗證管理原則。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="6f0b0-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0b0-110">語法</span><span class="sxs-lookup"><span data-stu-id="6f0b0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="6f0b0-111">成員</span><span class="sxs-lookup"><span data-stu-id="6f0b0-111">Members</span></span>

<span data-ttu-id="6f0b0-112">**MDM \_ Policy \_ Config01 \_ Authentication02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f0b0-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="6f0b0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6f0b0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f0b0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="6f0b0-114">Properties</span></span>

<span data-ttu-id="6f0b0-115">**MDM \_ Policy \_ Config01 \_ Authentication02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6f0b0-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="6f0b0-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f0b0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6f0b0-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="6f0b0-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f0b0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6f0b0-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="6f0b0-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f0b0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6f0b0-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="6f0b0-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6f0b0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f0b0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f0b0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f0b0-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="6f0b0-133">此類別的字串為 "Authentication"。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="6f0b0-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f0b0-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f0b0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f0b0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f0b0-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f0b0-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6f0b0-138">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="6f0b0-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="6f0b0-139">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="6f0b0-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f0b0-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f0b0-140">Requirements</span></span>



| <span data-ttu-id="6f0b0-141">需求</span><span class="sxs-lookup"><span data-stu-id="6f0b0-141">Requirement</span></span> | <span data-ttu-id="6f0b0-142">值</span><span class="sxs-lookup"><span data-stu-id="6f0b0-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0b0-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f0b0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6f0b0-144">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f0b0-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f0b0-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f0b0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6f0b0-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="6f0b0-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6f0b0-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f0b0-147">Namespace</span></span><br/>                | <span data-ttu-id="6f0b0-148">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="6f0b0-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6f0b0-149">MOF</span><span class="sxs-lookup"><span data-stu-id="6f0b0-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f0b0-150"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f0b0-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f0b0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6f0b0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f0b0-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f0b0-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f0b0-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f0b0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0b0-154">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="6f0b0-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

