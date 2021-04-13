---
title: MDM_Policy_Config01_ApplicationDefaults02 類別
description: MDM \_ Policy \_ Config01 \_ ApplicationDefaults02 類別可讓系統管理員設定預設檔案類型和通訊協定關聯。 設定時，將會在登入電腦時套用預設關聯。
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- MDM_Policy_Config01_ApplicationDefaults02 類別
- MDM_Policy_Config01_ApplicationDefaults02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464853"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="c6c49-106">MDM \_ 原則 \_ Config01 \_ ApplicationDefaults02 類別</span><span class="sxs-lookup"><span data-stu-id="c6c49-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="c6c49-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c6c49-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6c49-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c6c49-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6c49-109">MDM \_ Policy \_ Config01 \_ ApplicationDefaults02 類別可讓系統管理員設定預設檔案類型和通訊協定關聯。</span><span class="sxs-lookup"><span data-stu-id="c6c49-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="c6c49-110">設定時，將會在登入電腦時套用預設關聯。</span><span class="sxs-lookup"><span data-stu-id="c6c49-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="c6c49-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6c49-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c49-112">語法</span><span class="sxs-lookup"><span data-stu-id="c6c49-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="c6c49-113">成員</span><span class="sxs-lookup"><span data-stu-id="c6c49-113">Members</span></span>

<span data-ttu-id="c6c49-114">**MDM \_ Policy \_ Config01 \_ ApplicationDefaults02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c6c49-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="c6c49-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c6c49-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6c49-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c6c49-116">Properties</span></span>

<span data-ttu-id="c6c49-117">**MDM \_ Policy \_ Config01 \_ ApplicationDefaults02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c6c49-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c6c49-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6c49-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c49-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6c49-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6c49-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c6c49-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6c49-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c6c49-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c49-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6c49-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6c49-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6c49-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c49-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6c49-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6c49-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c6c49-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6c49-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6c49-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6c49-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6c49-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6c49-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6c49-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6c49-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6c49-129">Requirements</span></span>



| <span data-ttu-id="c6c49-130">需求</span><span class="sxs-lookup"><span data-stu-id="c6c49-130">Requirement</span></span> | <span data-ttu-id="c6c49-131">值</span><span class="sxs-lookup"><span data-stu-id="c6c49-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c49-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6c49-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c49-133">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6c49-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6c49-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6c49-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c49-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="c6c49-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c6c49-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="c6c49-136">Namespace</span></span><br/>                | <span data-ttu-id="c6c49-137">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c6c49-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c6c49-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c6c49-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6c49-139"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6c49-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6c49-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c6c49-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6c49-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6c49-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

