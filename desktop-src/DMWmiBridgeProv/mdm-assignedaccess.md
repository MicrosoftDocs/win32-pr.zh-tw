---
title: MDM_AssignedAccess 類別
description: MDM \_ >assignedaccess 類別可用來將裝置設定為以 kiosk 模式執行。
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- MDM_AssignedAccess 類別
- MDM_AssignedAccess 類別，描述
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466880"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="4f395-105">MDM \_ >assignedaccess 類別</span><span class="sxs-lookup"><span data-stu-id="4f395-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="4f395-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="4f395-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f395-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="4f395-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4f395-108">**MDM \_ >assignedaccess** 類別可用來將裝置設定為以 kiosk 模式執行。</span><span class="sxs-lookup"><span data-stu-id="4f395-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="4f395-109">一旦執行類別之後，與 kiosk 模式相關聯的下一個使用者登入，就會將裝置置於執行布建套件中所指定應用程式的 kiosk 模式中。</span><span class="sxs-lookup"><span data-stu-id="4f395-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="4f395-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f395-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f395-111">語法</span><span class="sxs-lookup"><span data-stu-id="4f395-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="4f395-112">成員</span><span class="sxs-lookup"><span data-stu-id="4f395-112">Members</span></span>

<span data-ttu-id="4f395-113">**MDM \_ >assignedaccess** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f395-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="4f395-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4f395-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f395-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4f395-115">Properties</span></span>

<span data-ttu-id="4f395-116">**MDM \_ >assignedaccess** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f395-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4f395-117">Configuration</span><span class="sxs-lookup"><span data-stu-id="4f395-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f395-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f395-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f395-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4f395-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f395-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4f395-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f395-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f395-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f395-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f395-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f395-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f395-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f395-124">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f395-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="4f395-125">此類別的字串為 ">assignedaccess"。</span><span class="sxs-lookup"><span data-stu-id="4f395-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="4f395-126">KioskModeApp</span><span class="sxs-lookup"><span data-stu-id="4f395-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f395-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f395-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f395-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4f395-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f395-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4f395-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f395-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4f395-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f395-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f395-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f395-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4f395-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4f395-133">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4f395-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="4f395-134">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="4f395-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f395-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f395-135">Requirements</span></span>



| <span data-ttu-id="4f395-136">需求</span><span class="sxs-lookup"><span data-stu-id="4f395-136">Requirement</span></span> | <span data-ttu-id="4f395-137">值</span><span class="sxs-lookup"><span data-stu-id="4f395-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f395-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f395-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4f395-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f395-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f395-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f395-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4f395-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="4f395-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4f395-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="4f395-142">Namespace</span></span><br/>                | <span data-ttu-id="4f395-143">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="4f395-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4f395-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4f395-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f395-145"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f395-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f395-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4f395-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f395-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f395-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f395-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f395-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f395-149">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="4f395-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

