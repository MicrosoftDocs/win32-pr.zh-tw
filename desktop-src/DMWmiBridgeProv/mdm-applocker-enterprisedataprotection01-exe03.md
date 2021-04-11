---
title: MDM_AppLocker_EnterpriseDataProtection01_EXE03 類別
description: MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03 類別會捕捉可執行檔應用程式清單，這些應用程式可處理企業資料。
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 類別
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106151"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="14ea8-105">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03 類別</span><span class="sxs-lookup"><span data-stu-id="14ea8-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="14ea8-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="14ea8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="14ea8-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="14ea8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="14ea8-108">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** 類別會捕捉可執行檔應用程式清單，這些應用程式可處理企業資料。</span><span class="sxs-lookup"><span data-stu-id="14ea8-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="14ea8-109">應該與/Vendor/MSFT/Policy/ConfigSource/DataProtection 中的設定一起使用。</span><span class="sxs-lookup"><span data-stu-id="14ea8-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="14ea8-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="14ea8-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ea8-111">語法</span><span class="sxs-lookup"><span data-stu-id="14ea8-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="14ea8-112">成員</span><span class="sxs-lookup"><span data-stu-id="14ea8-112">Members</span></span>

<span data-ttu-id="14ea8-113">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="14ea8-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="14ea8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="14ea8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14ea8-115">屬性</span><span class="sxs-lookup"><span data-stu-id="14ea8-115">Properties</span></span>

<span data-ttu-id="14ea8-116">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="14ea8-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14ea8-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="14ea8-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ea8-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14ea8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ea8-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="14ea8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14ea8-120">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14ea8-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="14ea8-121">定義啟動可執行應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="14ea8-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="14ea8-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="14ea8-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ea8-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14ea8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ea8-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="14ea8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14ea8-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14ea8-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="14ea8-126">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="14ea8-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="14ea8-127">針對此類別，字串為 "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*群組*"</span><span class="sxs-lookup"><span data-stu-id="14ea8-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="14ea8-128">**原則**</span><span class="sxs-lookup"><span data-stu-id="14ea8-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14ea8-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14ea8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14ea8-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14ea8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14ea8-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="14ea8-131">Requirements</span></span>



| <span data-ttu-id="14ea8-132">需求</span><span class="sxs-lookup"><span data-stu-id="14ea8-132">Requirement</span></span> | <span data-ttu-id="14ea8-133">值</span><span class="sxs-lookup"><span data-stu-id="14ea8-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14ea8-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14ea8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="14ea8-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14ea8-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14ea8-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14ea8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="14ea8-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="14ea8-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="14ea8-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="14ea8-138">Namespace</span></span><br/>                | <span data-ttu-id="14ea8-139">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="14ea8-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="14ea8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="14ea8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14ea8-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="14ea8-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="14ea8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="14ea8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14ea8-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ea8-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ea8-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14ea8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ea8-145">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="14ea8-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

