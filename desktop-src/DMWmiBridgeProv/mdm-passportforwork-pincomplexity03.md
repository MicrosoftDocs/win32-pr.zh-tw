---
title: MDM_PassportForWork_PINComplexity03 類別
description: MDM \_ PassportForWork \_ PINComplexity03 類別會針對 Windows Hello 企業版的登入認證定義 PIN 複雜性。
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- MDM_PassportForWork_PINComplexity03 類別
- MDM_PassportForWork_PINComplexity03 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934183"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="ec588-105">MDM \_ PassportForWork \_ PINComplexity03 類別</span><span class="sxs-lookup"><span data-stu-id="ec588-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="ec588-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ec588-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ec588-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ec588-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ec588-108">**MDM \_ PassportForWork \_ PINComplexity03** 類別會針對 Windows Hello 企業版的登入認證定義 PIN 複雜性。</span><span class="sxs-lookup"><span data-stu-id="ec588-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="ec588-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec588-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec588-110">語法</span><span class="sxs-lookup"><span data-stu-id="ec588-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="ec588-111">成員</span><span class="sxs-lookup"><span data-stu-id="ec588-111">Members</span></span>

<span data-ttu-id="ec588-112">**MDM \_ PassportForWork \_ PINComplexity03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec588-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="ec588-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ec588-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec588-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ec588-114">Properties</span></span>

<span data-ttu-id="ec588-115">**MDM \_ PassportForWork \_ PINComplexity03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ec588-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ec588-116">數位</span><span class="sxs-lookup"><span data-stu-id="ec588-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ec588-119">到期</span><span class="sxs-lookup"><span data-stu-id="ec588-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ec588-122">History</span><span class="sxs-lookup"><span data-stu-id="ec588-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec588-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ec588-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec588-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec588-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec588-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec588-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec588-129">PIN 原則的根節點。</span><span class="sxs-lookup"><span data-stu-id="ec588-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="ec588-130">LowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="ec588-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-131">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ec588-133">MaximumPINLength</span><span class="sxs-lookup"><span data-stu-id="ec588-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-134">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ec588-136">MinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="ec588-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-137">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec588-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ec588-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec588-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec588-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec588-142">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec588-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec588-143">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ec588-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="ec588-144">針對此類別，字串為 "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span><span class="sxs-lookup"><span data-stu-id="ec588-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="ec588-145">SpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="ec588-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-146">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ec588-148">UppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="ec588-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec588-149">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec588-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec588-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec588-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec588-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec588-151">Requirements</span></span>



| <span data-ttu-id="ec588-152">需求</span><span class="sxs-lookup"><span data-stu-id="ec588-152">Requirement</span></span> | <span data-ttu-id="ec588-153">值</span><span class="sxs-lookup"><span data-stu-id="ec588-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec588-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec588-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ec588-155">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec588-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec588-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec588-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ec588-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="ec588-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ec588-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec588-158">Namespace</span></span><br/>                | <span data-ttu-id="ec588-159">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ec588-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ec588-160">MOF</span><span class="sxs-lookup"><span data-stu-id="ec588-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec588-161"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec588-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec588-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ec588-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec588-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec588-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec588-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec588-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec588-165">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="ec588-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

