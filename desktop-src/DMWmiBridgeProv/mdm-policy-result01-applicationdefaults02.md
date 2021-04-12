---
title: MDM_Policy_Result01_ApplicationDefaults02 類別
description: MDM \_ Policy \_ Result01 \_ ApplicationDefaults02 類別代表可用的應用程式預設原則。
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- MDM_Policy_Result01_ApplicationDefaults02 類別
- MDM_Policy_Result01_ApplicationDefaults02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103884"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="948b5-105">MDM \_ 原則 \_ Result01 \_ ApplicationDefaults02 類別</span><span class="sxs-lookup"><span data-stu-id="948b5-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="948b5-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="948b5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="948b5-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="948b5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="948b5-108">MDM \_ Policy \_ Result01 \_ ApplicationDefaults02 類別代表可用的應用程式預設原則。</span><span class="sxs-lookup"><span data-stu-id="948b5-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="948b5-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="948b5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="948b5-110">語法</span><span class="sxs-lookup"><span data-stu-id="948b5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="948b5-111">成員</span><span class="sxs-lookup"><span data-stu-id="948b5-111">Members</span></span>

<span data-ttu-id="948b5-112">**MDM \_ Policy \_ Result01 \_ ApplicationDefaults02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="948b5-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="948b5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="948b5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="948b5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="948b5-114">Properties</span></span>

<span data-ttu-id="948b5-115">**MDM \_ Policy \_ Result01 \_ ApplicationDefaults02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="948b5-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="948b5-116">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="948b5-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948b5-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="948b5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="948b5-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="948b5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="948b5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="948b5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948b5-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="948b5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="948b5-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="948b5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="948b5-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="948b5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="948b5-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="948b5-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948b5-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="948b5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="948b5-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="948b5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="948b5-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="948b5-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="948b5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="948b5-127">Requirements</span></span>



| <span data-ttu-id="948b5-128">需求</span><span class="sxs-lookup"><span data-stu-id="948b5-128">Requirement</span></span> | <span data-ttu-id="948b5-129">值</span><span class="sxs-lookup"><span data-stu-id="948b5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948b5-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="948b5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="948b5-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="948b5-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="948b5-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="948b5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="948b5-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="948b5-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="948b5-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="948b5-134">Namespace</span></span><br/>                | <span data-ttu-id="948b5-135">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="948b5-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="948b5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="948b5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="948b5-137"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="948b5-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="948b5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="948b5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="948b5-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948b5-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

