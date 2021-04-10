---
title: MDM_Policy_Result01_Authentication02 類別
description: MDM \_ Policy \_ Result01 \_ Authentication02 類別代表可用的驗證管理原則。
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- MDM_Policy_Result01_Authentication02 類別
- MDM_Policy_Result01_Authentication02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106134"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="de462-105">MDM \_ 原則 \_ Result01 \_ Authentication02 類別</span><span class="sxs-lookup"><span data-stu-id="de462-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="de462-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="de462-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de462-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="de462-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de462-108">**MDM \_ Policy \_ Result01 \_ Authentication02** 類別代表可用的驗證管理原則。</span><span class="sxs-lookup"><span data-stu-id="de462-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="de462-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="de462-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de462-110">語法</span><span class="sxs-lookup"><span data-stu-id="de462-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="de462-111">成員</span><span class="sxs-lookup"><span data-stu-id="de462-111">Members</span></span>

<span data-ttu-id="de462-112">**MDM \_ Policy \_ Result01 \_ Authentication02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="de462-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="de462-113">屬性</span><span class="sxs-lookup"><span data-stu-id="de462-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de462-114">屬性</span><span class="sxs-lookup"><span data-stu-id="de462-114">Properties</span></span>

<span data-ttu-id="de462-115">**MDM \_ Policy \_ Result01 \_ Authentication02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="de462-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="de462-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="de462-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="de462-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de462-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="de462-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de462-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="de462-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="de462-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de462-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="de462-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de462-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="de462-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="de462-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de462-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="de462-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de462-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="de462-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="de462-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de462-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="de462-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de462-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de462-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de462-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de462-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de462-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de462-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de462-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de462-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="de462-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="de462-133">此類別的字串為 "Authentication"。</span><span class="sxs-lookup"><span data-stu-id="de462-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="de462-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="de462-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de462-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de462-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de462-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de462-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de462-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de462-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de462-138">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="de462-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="de462-139">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="de462-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de462-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="de462-140">Requirements</span></span>



| <span data-ttu-id="de462-141">需求</span><span class="sxs-lookup"><span data-stu-id="de462-141">Requirement</span></span> | <span data-ttu-id="de462-142">值</span><span class="sxs-lookup"><span data-stu-id="de462-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de462-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de462-143">Minimum supported client</span></span><br/> | <span data-ttu-id="de462-144">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de462-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de462-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de462-145">Minimum supported server</span></span><br/> | <span data-ttu-id="de462-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="de462-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de462-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="de462-147">Namespace</span></span><br/>                | <span data-ttu-id="de462-148">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="de462-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="de462-149">MOF</span><span class="sxs-lookup"><span data-stu-id="de462-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de462-150"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="de462-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de462-151">DLL</span><span class="sxs-lookup"><span data-stu-id="de462-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de462-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de462-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de462-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de462-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de462-154">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="de462-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

