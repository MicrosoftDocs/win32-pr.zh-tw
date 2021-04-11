---
title: MDM_Update_ApprovedUpdates01_01 類別
description: MDM \_ Update \_ ApprovedUpdates01 \_ 01 類別可用來管理和控制已核准更新的推出。
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- MDM_Update_ApprovedUpdates01_01 類別
- MDM_Update_ApprovedUpdates01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933944"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="fd1d3-105">MDM \_ Update \_ ApprovedUpdates01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="fd1d3-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="fd1d3-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd1d3-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fd1d3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd1d3-108">**MDM \_ Update \_ ApprovedUpdates01 \_ 01** 類別可用來管理和控制已核准更新的推出。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="fd1d3-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1d3-110">語法</span><span class="sxs-lookup"><span data-stu-id="fd1d3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="fd1d3-111">成員</span><span class="sxs-lookup"><span data-stu-id="fd1d3-111">Members</span></span>

<span data-ttu-id="fd1d3-112">**MDM \_ Update \_ ApprovedUpdates01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd1d3-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fd1d3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fd1d3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd1d3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fd1d3-114">Properties</span></span>

<span data-ttu-id="fd1d3-115">**MDM \_ Update \_ ApprovedUpdates01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd1d3-116">ApprovedTime</span><span class="sxs-lookup"><span data-stu-id="fd1d3-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd1d3-117">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fd1d3-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd1d3-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd1d3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd1d3-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd1d3-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd1d3-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd1d3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd1d3-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd1d3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd1d3-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd1d3-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd1d3-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fd1d3-124">此類別的字串為已核准更新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="fd1d3-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fd1d3-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd1d3-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd1d3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd1d3-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd1d3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd1d3-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd1d3-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd1d3-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fd1d3-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fd1d3-130">此類別的字串為 "./Vendor/MSFT/Update/ApprovedUpdates"</span><span class="sxs-lookup"><span data-stu-id="fd1d3-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd1d3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd1d3-131">Requirements</span></span>



| <span data-ttu-id="fd1d3-132">需求</span><span class="sxs-lookup"><span data-stu-id="fd1d3-132">Requirement</span></span> | <span data-ttu-id="fd1d3-133">值</span><span class="sxs-lookup"><span data-stu-id="fd1d3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1d3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd1d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1d3-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd1d3-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd1d3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd1d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1d3-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd1d3-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fd1d3-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd1d3-138">Namespace</span></span><br/>                | <span data-ttu-id="fd1d3-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fd1d3-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fd1d3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fd1d3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd1d3-141"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd1d3-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="fd1d3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fd1d3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd1d3-143"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd1d3-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

