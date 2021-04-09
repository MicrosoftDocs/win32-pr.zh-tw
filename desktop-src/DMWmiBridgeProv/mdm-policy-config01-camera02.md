---
title: MDM_Policy_Config01_Camera02 類別
description: MDM \_ Policy \_ Config01 \_ Camera02 類別代表可用的相機原則。
ms.assetid: dd17c2bc-8c96-4f5e-a4d2-cf1d27a92eb7
keywords:
- MDM_Policy_Config01_Camera02 類別
- MDM_Policy_Config01_Camera02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Camera02
- MDM_Policy_Config01_Camera02.InstanceID
- MDM_Policy_Config01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 377a9eb695560d7bf93fd6a5d761b1e95202bf20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685775"
---
# <a name="mdm_policy_config01_camera02-class"></a><span data-ttu-id="73090-105">MDM \_ 原則 \_ Config01 \_ Camera02 類別</span><span class="sxs-lookup"><span data-stu-id="73090-105">MDM\_Policy\_Config01\_Camera02 class</span></span>

<span data-ttu-id="73090-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="73090-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="73090-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="73090-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="73090-108">**MDM \_ Policy \_ Config01 \_ Camera02** 類別代表可用的相機原則。</span><span class="sxs-lookup"><span data-stu-id="73090-108">The **MDM\_Policy\_Config01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="73090-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="73090-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73090-110">語法</span><span class="sxs-lookup"><span data-stu-id="73090-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="73090-111">成員</span><span class="sxs-lookup"><span data-stu-id="73090-111">Members</span></span>

<span data-ttu-id="73090-112">**MDM \_ Policy \_ Config01 \_ Camera02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="73090-112">The **MDM\_Policy\_Config01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="73090-113">屬性</span><span class="sxs-lookup"><span data-stu-id="73090-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73090-114">屬性</span><span class="sxs-lookup"><span data-stu-id="73090-114">Properties</span></span>

<span data-ttu-id="73090-115">**MDM \_ Policy \_ Config01 \_ Camera02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="73090-115">The **MDM\_Policy\_Config01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="73090-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="73090-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73090-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="73090-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="73090-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="73090-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73090-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73090-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73090-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73090-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73090-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="73090-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73090-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73090-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73090-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="73090-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="73090-124">此類別的字串為 "相機"。</span><span class="sxs-lookup"><span data-stu-id="73090-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="73090-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="73090-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73090-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73090-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73090-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="73090-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73090-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73090-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73090-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="73090-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="73090-130">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="73090-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73090-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="73090-131">Requirements</span></span>



| <span data-ttu-id="73090-132">需求</span><span class="sxs-lookup"><span data-stu-id="73090-132">Requirement</span></span> | <span data-ttu-id="73090-133">值</span><span class="sxs-lookup"><span data-stu-id="73090-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73090-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73090-134">Minimum supported client</span></span><br/> | <span data-ttu-id="73090-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73090-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73090-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73090-136">Minimum supported server</span></span><br/> | <span data-ttu-id="73090-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="73090-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="73090-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="73090-138">Namespace</span></span><br/>                | <span data-ttu-id="73090-139">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="73090-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="73090-140">MOF</span><span class="sxs-lookup"><span data-stu-id="73090-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73090-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="73090-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="73090-142">DLL</span><span class="sxs-lookup"><span data-stu-id="73090-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73090-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73090-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73090-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73090-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73090-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="73090-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

