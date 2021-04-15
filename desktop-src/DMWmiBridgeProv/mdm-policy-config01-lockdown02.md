---
title: MDM_Policy_Config01_LockDown02 類別
description: MDM \_ Policy \_ Config01 \_ Lockdown02 類別代表可用的鎖定原則。
ms.assetid: 1d744400-70db-4f6b-97d0-7799fdfda44f
keywords:
- MDM_Policy_Config01_LockDown02 類別
- MDM_Policy_Config01_LockDown02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02.InstanceID
- MDM_Policy_Config01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf9914573c1a3f693d88da8b35b2d577e1f21f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465240"
---
# <a name="mdm_policy_config01_lockdown02-class"></a><span data-ttu-id="ad06f-105">MDM \_ 原則 \_ Config01 \_ LockDown02 類別</span><span class="sxs-lookup"><span data-stu-id="ad06f-105">MDM\_Policy\_Config01\_LockDown02 class</span></span>

<span data-ttu-id="ad06f-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ad06f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad06f-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ad06f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad06f-108">**MDM \_ Policy \_ Config01 \_ Lockdown02** 類別代表可用的鎖定原則。</span><span class="sxs-lookup"><span data-stu-id="ad06f-108">The **MDM\_Policy\_Config01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="ad06f-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad06f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad06f-110">語法</span><span class="sxs-lookup"><span data-stu-id="ad06f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="ad06f-111">成員</span><span class="sxs-lookup"><span data-stu-id="ad06f-111">Members</span></span>

<span data-ttu-id="ad06f-112">**MDM \_ Policy \_ Config01 \_ LockDown02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad06f-112">The **MDM\_Policy\_Config01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="ad06f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ad06f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad06f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ad06f-114">Properties</span></span>

<span data-ttu-id="ad06f-115">**MDM \_ Policy \_ Config01 \_ LockDown02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ad06f-115">The **MDM\_Policy\_Config01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ad06f-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="ad06f-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad06f-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad06f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad06f-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad06f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad06f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad06f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad06f-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad06f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad06f-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad06f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad06f-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad06f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad06f-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad06f-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ad06f-124">此類別的字串為「鎖定」。</span><span class="sxs-lookup"><span data-stu-id="ad06f-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="ad06f-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ad06f-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad06f-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad06f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad06f-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad06f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad06f-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad06f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad06f-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ad06f-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="ad06f-130">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="ad06f-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad06f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad06f-131">Requirements</span></span>



| <span data-ttu-id="ad06f-132">需求</span><span class="sxs-lookup"><span data-stu-id="ad06f-132">Requirement</span></span> | <span data-ttu-id="ad06f-133">值</span><span class="sxs-lookup"><span data-stu-id="ad06f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad06f-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad06f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ad06f-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad06f-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ad06f-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad06f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ad06f-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="ad06f-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ad06f-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad06f-138">Namespace</span></span><br/>                | <span data-ttu-id="ad06f-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ad06f-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ad06f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ad06f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad06f-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad06f-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="ad06f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ad06f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad06f-143"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad06f-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

