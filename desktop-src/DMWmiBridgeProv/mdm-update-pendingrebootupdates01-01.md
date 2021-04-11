---
title: MDM_Update_PendingRebootUpdates01_01 類別
description: MDM \_ Update \_ PendingRebootUpdates01 \_ 01 類別可用來管理在重新開機時擱置的更新。
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- MDM_Update_PendingRebootUpdates01_01 類別
- MDM_Update_PendingRebootUpdates01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca640a4de00ea9eb115b999129a16dd0bf930cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105719"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a><span data-ttu-id="fde53-105">MDM \_ Update \_ PendingRebootUpdates01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="fde53-105">MDM\_Update\_PendingRebootUpdates01\_01 class</span></span>

<span data-ttu-id="fde53-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fde53-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fde53-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fde53-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fde53-108">**MDM \_ Update \_ PendingRebootUpdates01 \_ 01** 類別可用來管理在重新開機時擱置的更新。</span><span class="sxs-lookup"><span data-stu-id="fde53-108">The **MDM\_Update\_PendingRebootUpdates01\_01** class is used to manage updates that are pending on reboot.</span></span>

<span data-ttu-id="fde53-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fde53-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde53-110">語法</span><span class="sxs-lookup"><span data-stu-id="fde53-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a><span data-ttu-id="fde53-111">成員</span><span class="sxs-lookup"><span data-stu-id="fde53-111">Members</span></span>

<span data-ttu-id="fde53-112">**MDM \_ Update \_ PendingRebootUpdates01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fde53-112">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fde53-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fde53-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fde53-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fde53-114">Properties</span></span>

<span data-ttu-id="fde53-115">**MDM \_ Update \_ PendingRebootUpdates01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fde53-115">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fde53-116">InstalledTime</span><span class="sxs-lookup"><span data-stu-id="fde53-116">InstalledTime</span></span>](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde53-117">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fde53-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fde53-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fde53-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fde53-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fde53-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde53-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fde53-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde53-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fde53-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde53-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fde53-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fde53-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fde53-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fde53-124">針對此類別，字串為擱置重新開機之更新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fde53-124">For this class, the string is the GUID of the update that is pending reboot.</span></span>

</dd> <dt>

<span data-ttu-id="fde53-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fde53-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fde53-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fde53-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fde53-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fde53-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fde53-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fde53-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fde53-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fde53-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fde53-130">此類別的字串為 "./Vendor/MSFT/Update/PendingRebootUpdates"</span><span class="sxs-lookup"><span data-stu-id="fde53-130">For this class, the string is "./Vendor/MSFT/Update/PendingRebootUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fde53-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fde53-131">Requirements</span></span>



| <span data-ttu-id="fde53-132">需求</span><span class="sxs-lookup"><span data-stu-id="fde53-132">Requirement</span></span> | <span data-ttu-id="fde53-133">值</span><span class="sxs-lookup"><span data-stu-id="fde53-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde53-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fde53-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fde53-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fde53-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fde53-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fde53-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fde53-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="fde53-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fde53-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="fde53-138">Namespace</span></span><br/>                | <span data-ttu-id="fde53-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fde53-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fde53-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fde53-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fde53-141"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fde53-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="fde53-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fde53-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde53-143"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde53-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

