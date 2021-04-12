---
title: MDM_Policy_Result01_Display02 類別
description: MDM \_ Policy \_ Result01 \_ Display02 類別代表顯示原則。
ms.assetid: 9f8675d6-1fd7-4269-8059-9159622f03cb
keywords:
- MDM_Policy_Result01_Display02 類別
- MDM_Policy_Result01_Display02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02.InstanceID
- MDM_Policy_Result01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b8097d943e92343250802d63c4dfa2e5c77920
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465436"
---
# <a name="mdm_policy_result01_display02-class"></a><span data-ttu-id="d45f8-105">MDM \_ 原則 \_ Result01 \_ Display02 類別</span><span class="sxs-lookup"><span data-stu-id="d45f8-105">MDM\_Policy\_Result01\_Display02 class</span></span>

<span data-ttu-id="d45f8-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d45f8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d45f8-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d45f8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d45f8-108">MDM \_ Policy \_ Result01 \_ Display02 類別代表顯示原則。</span><span class="sxs-lookup"><span data-stu-id="d45f8-108">The MDM\_Policy\_Result01\_Display02 class represents the display policies.</span></span>

<span data-ttu-id="d45f8-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d45f8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45f8-110">語法</span><span class="sxs-lookup"><span data-stu-id="d45f8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="d45f8-111">成員</span><span class="sxs-lookup"><span data-stu-id="d45f8-111">Members</span></span>

<span data-ttu-id="d45f8-112">**MDM \_ Policy \_ Result01 \_ Display02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d45f8-112">The **MDM\_Policy\_Result01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="d45f8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d45f8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d45f8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d45f8-114">Properties</span></span>

<span data-ttu-id="d45f8-115">**MDM \_ Policy \_ Result01 \_ Display02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d45f8-115">The **MDM\_Policy\_Result01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d45f8-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d45f8-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d45f8-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d45f8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d45f8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d45f8-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d45f8-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d45f8-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d45f8-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d45f8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d45f8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d45f8-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d45f8-124">TurnOffGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="d45f8-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d45f8-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d45f8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d45f8-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d45f8-127">TurnOnGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="d45f8-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d45f8-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d45f8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d45f8-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d45f8-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d45f8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d45f8-130">Requirements</span></span>



| <span data-ttu-id="d45f8-131">需求</span><span class="sxs-lookup"><span data-stu-id="d45f8-131">Requirement</span></span> | <span data-ttu-id="d45f8-132">值</span><span class="sxs-lookup"><span data-stu-id="d45f8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d45f8-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d45f8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d45f8-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d45f8-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d45f8-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d45f8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d45f8-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="d45f8-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d45f8-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="d45f8-137">Namespace</span></span><br/>                | <span data-ttu-id="d45f8-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d45f8-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d45f8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d45f8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d45f8-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d45f8-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d45f8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d45f8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d45f8-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d45f8-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

