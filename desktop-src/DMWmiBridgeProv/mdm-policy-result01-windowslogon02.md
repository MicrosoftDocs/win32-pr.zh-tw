---
title: MDM_Policy_Result01_WindowsLogon02 類別
description: MDM \_ Policy \_ Result01 \_ WindowsLogon02 類別會在登入時取得鎖定畫面和網路使用者介面的設定。
ms.assetid: 4c710e3d-e7d5-4e6e-ad99-b3c7d1813599
keywords:
- MDM_Policy_Result01_WindowsLogon02 類別
- MDM_Policy_Result01_WindowsLogon02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02.InstanceID
- MDM_Policy_Result01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e9c0e2ebc2e82d5daef174ce9322b5b4b5ec7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093916"
---
# <a name="mdm_policy_result01_windowslogon02-class"></a><span data-ttu-id="09ea5-105">MDM \_ 原則 \_ Result01 \_ WindowsLogon02 類別</span><span class="sxs-lookup"><span data-stu-id="09ea5-105">MDM\_Policy\_Result01\_WindowsLogon02 class</span></span>

<span data-ttu-id="09ea5-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="09ea5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="09ea5-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="09ea5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="09ea5-108">MDM \_ Policy \_ Result01 \_ WindowsLogon02 類別會在登入時取得鎖定畫面和網路使用者介面的設定。</span><span class="sxs-lookup"><span data-stu-id="09ea5-108">The MDM\_Policy\_Result01\_WindowsLogon02 class gets the settings of the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="09ea5-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="09ea5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ea5-110">語法</span><span class="sxs-lookup"><span data-stu-id="09ea5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="09ea5-111">成員</span><span class="sxs-lookup"><span data-stu-id="09ea5-111">Members</span></span>

<span data-ttu-id="09ea5-112">**MDM \_ Policy \_ Result01 \_ WindowsLogon02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="09ea5-112">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="09ea5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="09ea5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09ea5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="09ea5-114">Properties</span></span>

<span data-ttu-id="09ea5-115">**MDM \_ Policy \_ Result01 \_ WindowsLogon02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="09ea5-115">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="09ea5-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="09ea5-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09ea5-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09ea5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="09ea5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09ea5-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="09ea5-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09ea5-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09ea5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="09ea5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09ea5-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="09ea5-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09ea5-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="09ea5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="09ea5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09ea5-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09ea5-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09ea5-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09ea5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09ea5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09ea5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09ea5-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="09ea5-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09ea5-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="09ea5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="09ea5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09ea5-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09ea5-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09ea5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="09ea5-133">Requirements</span></span>



| <span data-ttu-id="09ea5-134">需求</span><span class="sxs-lookup"><span data-stu-id="09ea5-134">Requirement</span></span> | <span data-ttu-id="09ea5-135">值</span><span class="sxs-lookup"><span data-stu-id="09ea5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ea5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09ea5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="09ea5-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09ea5-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09ea5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09ea5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="09ea5-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="09ea5-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="09ea5-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="09ea5-140">Namespace</span></span><br/>                | <span data-ttu-id="09ea5-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="09ea5-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="09ea5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="09ea5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09ea5-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="09ea5-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="09ea5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="09ea5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09ea5-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ea5-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

