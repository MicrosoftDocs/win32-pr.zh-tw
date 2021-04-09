---
title: MDM_PassportForWork_Biometrics01 類別
description: MDM \_ PassportForWork \_ Biometrics01 類別會定義生物特徵辨識設定。
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- MDM_PassportForWork_Biometrics01 類別
- MDM_PassportForWork_Biometrics01 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094279"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="0d058-105">MDM \_ PassportForWork \_ Biometrics01 類別</span><span class="sxs-lookup"><span data-stu-id="0d058-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="0d058-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0d058-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0d058-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0d058-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0d058-108">**MDM \_ PassportForWork \_ Biometrics01** 類別會定義生物特徵辨識設定。</span><span class="sxs-lookup"><span data-stu-id="0d058-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="0d058-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d058-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d058-110">語法</span><span class="sxs-lookup"><span data-stu-id="0d058-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="0d058-111">成員</span><span class="sxs-lookup"><span data-stu-id="0d058-111">Members</span></span>

<span data-ttu-id="0d058-112">**MDM \_ PassportForWork \_ Biometrics01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0d058-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="0d058-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0d058-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d058-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0d058-114">Properties</span></span>

<span data-ttu-id="0d058-115">**MDM \_ PassportForWork \_ Biometrics01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0d058-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0d058-116">FacialFeaturesUseEnhancedAntiSpoofing</span><span class="sxs-lookup"><span data-stu-id="0d058-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d058-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0d058-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d058-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d058-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d058-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0d058-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d058-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d058-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d058-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d058-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d058-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d058-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d058-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d058-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="0d058-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0d058-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d058-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0d058-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d058-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0d058-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d058-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d058-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d058-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0d058-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="0d058-129">此類別的字串為 "./Vendor/MSFT/PassportForWork/"</span><span class="sxs-lookup"><span data-stu-id="0d058-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="0d058-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="0d058-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d058-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0d058-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d058-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0d058-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d058-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d058-133">Requirements</span></span>



| <span data-ttu-id="0d058-134">需求</span><span class="sxs-lookup"><span data-stu-id="0d058-134">Requirement</span></span> | <span data-ttu-id="0d058-135">值</span><span class="sxs-lookup"><span data-stu-id="0d058-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d058-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d058-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0d058-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d058-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d058-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d058-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0d058-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d058-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0d058-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d058-140">Namespace</span></span><br/>                | <span data-ttu-id="0d058-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0d058-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0d058-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0d058-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d058-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d058-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d058-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0d058-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d058-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d058-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d058-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d058-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d058-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="0d058-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

