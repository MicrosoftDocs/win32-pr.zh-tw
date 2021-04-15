---
title: MDM_Policy_Result01_BitLocker02 類別
description: MDM \_ Policy \_ Result01 \_ Bitlocker02 類別代表可用的 BitLocker 原則。
ms.assetid: 5b20a129-65a8-4ec1-b938-57ddaca46ac3
keywords:
- MDM_Policy_Result01_BitLocker02 類別
- MDM_Policy_Result01_BitLocker02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02.InstanceID
- MDM_Policy_Result01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b063ab67411d8be7fc4c819934b63c0af0096ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466877"
---
# <a name="mdm_policy_result01_bitlocker02-class"></a><span data-ttu-id="9f9a4-105">MDM \_ 原則 \_ Result01 \_ BitLocker02 類別</span><span class="sxs-lookup"><span data-stu-id="9f9a4-105">MDM\_Policy\_Result01\_BitLocker02 class</span></span>

<span data-ttu-id="9f9a4-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f9a4-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="9f9a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f9a4-108">**MDM \_ Policy \_ Result01 \_ Bitlocker02** 類別代表可用的 BitLocker 原則。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-108">The **MDM\_Policy\_Result01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="9f9a4-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9a4-110">語法</span><span class="sxs-lookup"><span data-stu-id="9f9a4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="9f9a4-111">成員</span><span class="sxs-lookup"><span data-stu-id="9f9a4-111">Members</span></span>

<span data-ttu-id="9f9a4-112">**MDM \_ Policy \_ Result01 \_ BitLocker02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f9a4-112">The **MDM\_Policy\_Result01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="9f9a4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9f9a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f9a4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9f9a4-114">Properties</span></span>

<span data-ttu-id="9f9a4-115">**MDM \_ Policy \_ Result01 \_ BitLocker02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-115">The **MDM\_Policy\_Result01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f9a4-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="9f9a4-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9a4-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f9a4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f9a4-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f9a4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f9a4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f9a4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9a4-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9f9a4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f9a4-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9f9a4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f9a4-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f9a4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f9a4-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f9a4-124">此類別的字串為 "BitLocker"</span><span class="sxs-lookup"><span data-stu-id="9f9a4-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="9f9a4-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f9a4-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9a4-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9f9a4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f9a4-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9f9a4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f9a4-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f9a4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f9a4-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9f9a4-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f9a4-130">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="9f9a4-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f9a4-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f9a4-131">Requirements</span></span>



| <span data-ttu-id="9f9a4-132">需求</span><span class="sxs-lookup"><span data-stu-id="9f9a4-132">Requirement</span></span> | <span data-ttu-id="9f9a4-133">值</span><span class="sxs-lookup"><span data-stu-id="9f9a4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9a4-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f9a4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9a4-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f9a4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f9a4-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f9a4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9a4-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f9a4-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f9a4-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f9a4-138">Namespace</span></span><br/>                | <span data-ttu-id="9f9a4-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9f9a4-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9f9a4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9f9a4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f9a4-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f9a4-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f9a4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9f9a4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f9a4-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f9a4-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f9a4-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f9a4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9a4-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="9f9a4-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

