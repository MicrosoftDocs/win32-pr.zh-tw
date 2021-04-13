---
title: MDM_EnterpriseModernAppManagement_AppManagement01_02 類別
description: MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 類別指定您是否要封鎖特定應用程式，而不是透過自動更新進行更新。
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_02 類別
- MDM_EnterpriseModernAppManagement_AppManagement01_02 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466204"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="01c67-105">MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 類別</span><span class="sxs-lookup"><span data-stu-id="01c67-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="01c67-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="01c67-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01c67-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="01c67-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01c67-108">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** 類別指定您是否要封鎖特定應用程式，而不是透過自動更新進行更新。</span><span class="sxs-lookup"><span data-stu-id="01c67-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="01c67-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="01c67-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c67-110">語法</span><span class="sxs-lookup"><span data-stu-id="01c67-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="01c67-111">成員</span><span class="sxs-lookup"><span data-stu-id="01c67-111">Members</span></span>

<span data-ttu-id="01c67-112">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01c67-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="01c67-113">屬性</span><span class="sxs-lookup"><span data-stu-id="01c67-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01c67-114">屬性</span><span class="sxs-lookup"><span data-stu-id="01c67-114">Properties</span></span>

<span data-ttu-id="01c67-115">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01c67-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="01c67-116">DoNotUpdate</span><span class="sxs-lookup"><span data-stu-id="01c67-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c67-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01c67-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01c67-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01c67-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01c67-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01c67-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c67-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01c67-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c67-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01c67-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c67-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01c67-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01c67-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="01c67-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="01c67-124">針對這個類別，字串是套件系列名稱的實例。</span><span class="sxs-lookup"><span data-stu-id="01c67-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="01c67-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="01c67-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c67-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01c67-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c67-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01c67-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c67-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01c67-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01c67-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="01c67-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="01c67-130">針對此類別，字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span><span class="sxs-lookup"><span data-stu-id="01c67-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01c67-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="01c67-131">Requirements</span></span>



| <span data-ttu-id="01c67-132">需求</span><span class="sxs-lookup"><span data-stu-id="01c67-132">Requirement</span></span> | <span data-ttu-id="01c67-133">值</span><span class="sxs-lookup"><span data-stu-id="01c67-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c67-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01c67-134">Minimum supported client</span></span><br/> | <span data-ttu-id="01c67-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01c67-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01c67-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01c67-136">Minimum supported server</span></span><br/> | <span data-ttu-id="01c67-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="01c67-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="01c67-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="01c67-138">Namespace</span></span><br/>                | <span data-ttu-id="01c67-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="01c67-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="01c67-140">MOF</span><span class="sxs-lookup"><span data-stu-id="01c67-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01c67-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="01c67-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="01c67-142">DLL</span><span class="sxs-lookup"><span data-stu-id="01c67-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c67-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c67-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c67-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01c67-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c67-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="01c67-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

