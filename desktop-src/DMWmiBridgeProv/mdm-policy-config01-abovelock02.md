---
title: MDM_Policy_Config01_AboveLock02 類別
description: MDM \_ Policy \_ Config01 \_ AboveLock02 類別代表原則，可決定裝置鎖定畫面上所允許的動作。
ms.assetid: ad76e424-e5b6-46ba-a6a7-5dc00f983918
keywords:
- MDM_Policy_Config01_AboveLock02 類別
- MDM_Policy_Config01_AboveLock02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AboveLock02
- MDM_Policy_Config01_AboveLock02.InstanceID
- MDM_Policy_Config01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703971a10fe927c391831a9db65d270291b56e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967727"
---
# <a name="mdm_policy_config01_abovelock02-class"></a><span data-ttu-id="d1cde-105">MDM \_ 原則 \_ Config01 \_ AboveLock02 類別</span><span class="sxs-lookup"><span data-stu-id="d1cde-105">MDM\_Policy\_Config01\_AboveLock02 class</span></span>

<span data-ttu-id="d1cde-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d1cde-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d1cde-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d1cde-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d1cde-108">**MDM \_ Policy \_ Config01 \_ AboveLock02** 類別代表原則，可決定裝置鎖定畫面上所允許的動作。</span><span class="sxs-lookup"><span data-stu-id="d1cde-108">The **MDM\_Policy\_Config01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="d1cde-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d1cde-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cde-110">語法</span><span class="sxs-lookup"><span data-stu-id="d1cde-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="d1cde-111">成員</span><span class="sxs-lookup"><span data-stu-id="d1cde-111">Members</span></span>

<span data-ttu-id="d1cde-112">**MDM \_ Policy \_ Config01 \_ AboveLock02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d1cde-112">The **MDM\_Policy\_Config01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="d1cde-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d1cde-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1cde-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d1cde-114">Properties</span></span>

<span data-ttu-id="d1cde-115">**MDM \_ Policy \_ Config01 \_ AboveLock02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d1cde-115">The **MDM\_Policy\_Config01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d1cde-116">AllowCortanaAboveLock</span><span class="sxs-lookup"><span data-stu-id="d1cde-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cde-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d1cde-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cde-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1cde-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="d1cde-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cde-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d1cde-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cde-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1cde-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1cde-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cde-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1cde-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1cde-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1cde-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1cde-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1cde-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="d1cde-127">此類別的字串為 "AboveLock"。</span><span class="sxs-lookup"><span data-stu-id="d1cde-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="d1cde-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d1cde-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cde-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1cde-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1cde-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cde-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1cde-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1cde-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d1cde-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d1cde-133">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="d1cde-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1cde-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1cde-134">Requirements</span></span>



| <span data-ttu-id="d1cde-135">需求</span><span class="sxs-lookup"><span data-stu-id="d1cde-135">Requirement</span></span> | <span data-ttu-id="d1cde-136">值</span><span class="sxs-lookup"><span data-stu-id="d1cde-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cde-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1cde-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cde-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1cde-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1cde-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1cde-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cde-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="d1cde-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d1cde-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1cde-141">Namespace</span></span><br/>                | <span data-ttu-id="d1cde-142">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="d1cde-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d1cde-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d1cde-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1cde-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1cde-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1cde-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cde-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1cde-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cde-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cde-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1cde-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cde-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="d1cde-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

