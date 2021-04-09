---
title: MDM_Update 類別
description: MDM \_ Update 類別可用來管理和控制新更新的推出。
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- MDM_Update 類別
- MDM_Update 類別，描述
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843412"
---
# <a name="mdm_update-class"></a><span data-ttu-id="1ba28-105">MDM \_ 更新類別</span><span class="sxs-lookup"><span data-stu-id="1ba28-105">MDM\_Update class</span></span>

<span data-ttu-id="1ba28-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1ba28-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ba28-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1ba28-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ba28-108">**MDM \_ Update** 類別可用來管理和控制新更新的推出。</span><span class="sxs-lookup"><span data-stu-id="1ba28-108">The **MDM\_Update** class is used to manage and control the rollout of new updates.</span></span>

<span data-ttu-id="1ba28-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba28-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba28-110">語法</span><span class="sxs-lookup"><span data-stu-id="1ba28-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a><span data-ttu-id="1ba28-111">成員</span><span class="sxs-lookup"><span data-stu-id="1ba28-111">Members</span></span>

<span data-ttu-id="1ba28-112">**MDM \_ Update** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ba28-112">The **MDM\_Update** class has these types of members:</span></span>

-   [<span data-ttu-id="1ba28-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1ba28-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ba28-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1ba28-114">Properties</span></span>

<span data-ttu-id="1ba28-115">**MDM \_ 更新** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ba28-115">The **MDM\_Update** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1ba28-116">DeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="1ba28-116">DeferUpgrade</span></span>](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba28-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1ba28-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1ba28-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba28-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ba28-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba28-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ba28-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba28-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ba28-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ba28-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba28-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="1ba28-124">此類別的字串為 "Update"。</span><span class="sxs-lookup"><span data-stu-id="1ba28-124">For this class, the string is "Update".</span></span>

</dd> <dt>

[<span data-ttu-id="1ba28-125">LastSuccessfulScanTime</span><span class="sxs-lookup"><span data-stu-id="1ba28-125">LastSuccessfulScanTime</span></span>](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba28-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1ba28-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1ba28-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba28-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1ba28-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba28-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ba28-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ba28-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ba28-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ba28-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1ba28-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="1ba28-133">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="1ba28-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ba28-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ba28-134">Requirements</span></span>



| <span data-ttu-id="1ba28-135">需求</span><span class="sxs-lookup"><span data-stu-id="1ba28-135">Requirement</span></span> | <span data-ttu-id="1ba28-136">值</span><span class="sxs-lookup"><span data-stu-id="1ba28-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba28-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ba28-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba28-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ba28-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1ba28-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ba28-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba28-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="1ba28-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1ba28-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ba28-141">Namespace</span></span><br/>                | <span data-ttu-id="1ba28-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1ba28-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="1ba28-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1ba28-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ba28-144"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ba28-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="1ba28-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1ba28-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ba28-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ba28-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

