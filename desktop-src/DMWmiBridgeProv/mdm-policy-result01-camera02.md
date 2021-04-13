---
title: MDM_Policy_Result01_Camera02 類別
description: MDM \_ Policy \_ Result01 \_ Camera02 類別代表可用的相機原則。
ms.assetid: 72b11a00-6a34-4939-b1d0-e457b0c80c7f
keywords:
- MDM_Policy_Result01_Camera02 類別
- MDM_Policy_Result01_Camera02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Camera02
- MDM_Policy_Result01_Camera02.InstanceID
- MDM_Policy_Result01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9a266e93740cda5afbbc9a8195907a2a40cff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464645"
---
# <a name="mdm_policy_result01_camera02-class"></a><span data-ttu-id="e2588-105">MDM \_ 原則 \_ Result01 \_ Camera02 類別</span><span class="sxs-lookup"><span data-stu-id="e2588-105">MDM\_Policy\_Result01\_Camera02 class</span></span>

<span data-ttu-id="e2588-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e2588-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e2588-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e2588-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e2588-108">**MDM \_ Policy \_ Result01 \_ Camera02** 類別代表可用的相機原則。</span><span class="sxs-lookup"><span data-stu-id="e2588-108">The **MDM\_Policy\_Result01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="e2588-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2588-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2588-110">語法</span><span class="sxs-lookup"><span data-stu-id="e2588-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="e2588-111">成員</span><span class="sxs-lookup"><span data-stu-id="e2588-111">Members</span></span>

<span data-ttu-id="e2588-112">**MDM \_ Policy \_ Result01 \_ Camera02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e2588-112">The **MDM\_Policy\_Result01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="e2588-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e2588-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2588-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e2588-114">Properties</span></span>

<span data-ttu-id="e2588-115">**MDM \_ Policy \_ Result01 \_ Camera02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e2588-115">The **MDM\_Policy\_Result01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e2588-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="e2588-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2588-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e2588-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2588-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e2588-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2588-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2588-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2588-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2588-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2588-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2588-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2588-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2588-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2588-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2588-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e2588-124">此類別的字串為 "相機"。</span><span class="sxs-lookup"><span data-stu-id="e2588-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="e2588-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e2588-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2588-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2588-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2588-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2588-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2588-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2588-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2588-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e2588-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="e2588-130">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="e2588-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2588-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2588-131">Requirements</span></span>



| <span data-ttu-id="e2588-132">需求</span><span class="sxs-lookup"><span data-stu-id="e2588-132">Requirement</span></span> | <span data-ttu-id="e2588-133">值</span><span class="sxs-lookup"><span data-stu-id="e2588-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2588-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2588-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e2588-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2588-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2588-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2588-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e2588-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="e2588-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e2588-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2588-138">Namespace</span></span><br/>                | <span data-ttu-id="e2588-139">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="e2588-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e2588-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e2588-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2588-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2588-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2588-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e2588-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2588-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2588-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2588-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2588-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2588-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="e2588-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

