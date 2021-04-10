---
title: MDM_Policy_User_Config01_ApplicationManagement02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ ApplicationManagement02 類別代表以每個使用者為基礎所設定的啟動原則。
ms.assetid: 3dd20364-6723-4ed6-87c0-729789ddd948
keywords:
- MDM_Policy_User_Config01_ApplicationManagement02 類別
- MDM_Policy_User_Config01_ApplicationManagement02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88226122eefb3335ef1b19680268ea5acf1d5388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093915"
---
# <a name="mdm_policy_user_config01_applicationmanagement02-class"></a><span data-ttu-id="8726a-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ ApplicationManagement02 類別</span><span class="sxs-lookup"><span data-stu-id="8726a-105">MDM\_Policy\_User\_Config01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="8726a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="8726a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8726a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="8726a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8726a-108">**MDM \_ Policy \_ User \_ Config01 \_ ApplicationManagement02** 類別代表以每個使用者為基礎所設定的啟動原則。</span><span class="sxs-lookup"><span data-stu-id="8726a-108">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="8726a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8726a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8726a-110">語法</span><span class="sxs-lookup"><span data-stu-id="8726a-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="8726a-111">成員</span><span class="sxs-lookup"><span data-stu-id="8726a-111">Members</span></span>

<span data-ttu-id="8726a-112">**MDM \_ Policy \_ User \_ Config01 \_ ApplicationManagement02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8726a-112">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="8726a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8726a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8726a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8726a-114">Properties</span></span>

<span data-ttu-id="8726a-115">**MDM \_ Policy \_ User \_ Config01 \_ ApplicationManagement02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8726a-115">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8726a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8726a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8726a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8726a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8726a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8726a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8726a-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8726a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8726a-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="8726a-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="8726a-121">針對此類別，字串為 "ApplicationManagement"</span><span class="sxs-lookup"><span data-stu-id="8726a-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="8726a-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8726a-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8726a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8726a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8726a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8726a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8726a-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8726a-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8726a-126">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8726a-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="8726a-127">此類別的字串為 "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="8726a-127">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="8726a-128">RequirePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="8726a-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8726a-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="8726a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8726a-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8726a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8726a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="8726a-131">Requirements</span></span>



| <span data-ttu-id="8726a-132">需求</span><span class="sxs-lookup"><span data-stu-id="8726a-132">Requirement</span></span> | <span data-ttu-id="8726a-133">值</span><span class="sxs-lookup"><span data-stu-id="8726a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8726a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8726a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8726a-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8726a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8726a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8726a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8726a-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="8726a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8726a-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="8726a-138">Namespace</span></span><br/>                | <span data-ttu-id="8726a-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8726a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8726a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8726a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8726a-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8726a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8726a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8726a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8726a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8726a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8726a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8726a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8726a-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="8726a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

