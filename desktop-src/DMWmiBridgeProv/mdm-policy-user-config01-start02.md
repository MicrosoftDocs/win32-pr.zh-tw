---
title: MDM_Policy_User_Config01_Start02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ Start02 類別代表以每個使用者為基礎所設定的啟動原則。
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- MDM_Policy_User_Config01_Start02 類別
- MDM_Policy_User_Config01_Start02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384722"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="3ee37-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ Start02 類別</span><span class="sxs-lookup"><span data-stu-id="3ee37-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="3ee37-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3ee37-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3ee37-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3ee37-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3ee37-108">**MDM \_ Policy \_ User \_ Config01 \_ Start02** 類別代表以每個使用者為基礎所設定的啟動原則。</span><span class="sxs-lookup"><span data-stu-id="3ee37-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="3ee37-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3ee37-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee37-110">語法</span><span class="sxs-lookup"><span data-stu-id="3ee37-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="3ee37-111">成員</span><span class="sxs-lookup"><span data-stu-id="3ee37-111">Members</span></span>

<span data-ttu-id="3ee37-112">**MDM \_ Policy \_ User \_ Config01 \_ Start02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ee37-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="3ee37-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3ee37-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ee37-114">屬性</span><span class="sxs-lookup"><span data-stu-id="3ee37-114">Properties</span></span>

<span data-ttu-id="3ee37-115">**MDM \_ Policy \_ User \_ Config01 \_ Start02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3ee37-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3ee37-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="3ee37-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee37-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3ee37-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3ee37-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ee37-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ee37-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee37-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ee37-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ee37-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ee37-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3ee37-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ee37-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="3ee37-124">此類別的字串為 "Start"</span><span class="sxs-lookup"><span data-stu-id="3ee37-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="3ee37-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3ee37-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee37-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ee37-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ee37-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ee37-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3ee37-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3ee37-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="3ee37-130">此類別的字串為 "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="3ee37-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="3ee37-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="3ee37-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee37-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3ee37-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ee37-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3ee37-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ee37-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ee37-134">Requirements</span></span>



| <span data-ttu-id="3ee37-135">需求</span><span class="sxs-lookup"><span data-stu-id="3ee37-135">Requirement</span></span> | <span data-ttu-id="3ee37-136">值</span><span class="sxs-lookup"><span data-stu-id="3ee37-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee37-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ee37-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee37-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ee37-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ee37-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ee37-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee37-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ee37-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3ee37-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ee37-141">Namespace</span></span><br/>                | <span data-ttu-id="3ee37-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3ee37-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3ee37-143">MOF</span><span class="sxs-lookup"><span data-stu-id="3ee37-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ee37-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ee37-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ee37-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3ee37-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ee37-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ee37-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ee37-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ee37-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee37-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="3ee37-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

