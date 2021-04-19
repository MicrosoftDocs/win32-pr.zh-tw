---
title: MDM_ActiveSync_User_ContentTypes04_01 類別
description: MDM \_ ActiveSync \_ 使用者 \_ ContentTypes04 \_ 01 類別定義要個別啟用/停用同步處理的內容類型。
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- MDM_ActiveSync_User_ContentTypes04_01 類別
- MDM_ActiveSync_User_ContentTypes04_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968153"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="c2939-105">MDM \_ ActiveSync \_ 使用者 \_ ContentTypes04 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="c2939-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="c2939-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c2939-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2939-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c2939-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2939-108">**MDM \_ ActiveSync \_ 使用者 \_ ContentTypes04 \_ 01** 類別定義要個別啟用/停用同步處理的內容類型。</span><span class="sxs-lookup"><span data-stu-id="c2939-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="c2939-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2939-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2939-110">語法</span><span class="sxs-lookup"><span data-stu-id="c2939-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="c2939-111">成員</span><span class="sxs-lookup"><span data-stu-id="c2939-111">Members</span></span>

<span data-ttu-id="c2939-112">**MDM \_ ActiveSync \_ 使用者 \_ ContentTypes04 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c2939-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c2939-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c2939-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2939-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c2939-114">Properties</span></span>

<span data-ttu-id="c2939-115">**MDM \_ ActiveSync \_ 使用者 \_ ContentTypes04 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c2939-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c2939-116">Enabled</span><span class="sxs-lookup"><span data-stu-id="c2939-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2939-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2939-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2939-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c2939-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2939-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c2939-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2939-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2939-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2939-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2939-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2939-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2939-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2939-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2939-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="c2939-124">名稱</span><span class="sxs-lookup"><span data-stu-id="c2939-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2939-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2939-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2939-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c2939-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2939-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c2939-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2939-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c2939-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2939-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c2939-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2939-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c2939-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c2939-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="c2939-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="c2939-132">針對此類別，字串為 "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span><span class="sxs-lookup"><span data-stu-id="c2939-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2939-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2939-133">Requirements</span></span>



| <span data-ttu-id="c2939-134">需求</span><span class="sxs-lookup"><span data-stu-id="c2939-134">Requirement</span></span> | <span data-ttu-id="c2939-135">值</span><span class="sxs-lookup"><span data-stu-id="c2939-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2939-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2939-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c2939-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2939-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2939-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2939-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c2939-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="c2939-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c2939-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="c2939-140">Namespace</span></span><br/>                | <span data-ttu-id="c2939-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c2939-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c2939-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c2939-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2939-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2939-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2939-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c2939-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2939-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2939-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2939-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2939-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2939-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="c2939-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

