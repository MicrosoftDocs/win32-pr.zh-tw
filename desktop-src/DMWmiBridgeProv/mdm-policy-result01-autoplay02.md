---
title: MDM_Policy_Result01_Autoplay02 類別
description: MDM \_ Policy \_ Result01 \_ Autoplay02 類別代表可用的自動播放原則。
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- MDM_Policy_Result01_Autoplay02 類別
- MDM_Policy_Result01_Autoplay02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106128"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="73f96-105">MDM \_ 原則 \_ Result01 \_ Autoplay02 類別</span><span class="sxs-lookup"><span data-stu-id="73f96-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="73f96-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="73f96-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="73f96-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="73f96-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="73f96-108">MDM \_ Policy \_ Result01 \_ Autoplay02 類別代表可用的自動播放原則。</span><span class="sxs-lookup"><span data-stu-id="73f96-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="73f96-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="73f96-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f96-110">語法</span><span class="sxs-lookup"><span data-stu-id="73f96-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="73f96-111">成員</span><span class="sxs-lookup"><span data-stu-id="73f96-111">Members</span></span>

<span data-ttu-id="73f96-112">**MDM \_ Policy \_ Result01 \_ Autoplay02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="73f96-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="73f96-113">屬性</span><span class="sxs-lookup"><span data-stu-id="73f96-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73f96-114">屬性</span><span class="sxs-lookup"><span data-stu-id="73f96-114">Properties</span></span>

<span data-ttu-id="73f96-115">**MDM \_ Policy \_ Result01 \_ Autoplay02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="73f96-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="73f96-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="73f96-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f96-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73f96-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f96-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="73f96-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73f96-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73f96-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f96-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73f96-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f96-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="73f96-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f96-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73f96-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73f96-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="73f96-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f96-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73f96-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f96-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="73f96-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73f96-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73f96-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="73f96-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="73f96-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f96-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73f96-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f96-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="73f96-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="73f96-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="73f96-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73f96-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="73f96-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73f96-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="73f96-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73f96-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="73f96-133">Requirements</span></span>



| <span data-ttu-id="73f96-134">需求</span><span class="sxs-lookup"><span data-stu-id="73f96-134">Requirement</span></span> | <span data-ttu-id="73f96-135">值</span><span class="sxs-lookup"><span data-stu-id="73f96-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f96-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73f96-136">Minimum supported client</span></span><br/> | <span data-ttu-id="73f96-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73f96-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73f96-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73f96-138">Minimum supported server</span></span><br/> | <span data-ttu-id="73f96-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="73f96-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="73f96-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="73f96-140">Namespace</span></span><br/>                | <span data-ttu-id="73f96-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="73f96-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="73f96-142">MOF</span><span class="sxs-lookup"><span data-stu-id="73f96-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73f96-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="73f96-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="73f96-144">DLL</span><span class="sxs-lookup"><span data-stu-id="73f96-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f96-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73f96-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

