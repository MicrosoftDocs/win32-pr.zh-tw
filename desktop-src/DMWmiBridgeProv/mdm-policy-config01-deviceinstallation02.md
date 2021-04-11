---
title: MDM_Policy_Config01_DeviceInstallation02 類別
description: MDM \_ Policy \_ Config01 DeviceInstallation02 類別會設定 \_ 可用的裝置安裝原則。
ms.assetid: 6aa60809-d6c7-4dfb-9144-e5d69466f454
keywords:
- MDM_Policy_Config01_DeviceInstallation02 類別
- MDM_Policy_Config01_DeviceInstallation02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceInstallation02
- MDM_Policy_Config01_DeviceInstallation02.InstanceID
- MDM_Policy_Config01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79df6829f05a49ff5f16e3d8e0cd3dfabfc7bbf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843344"
---
# <a name="mdm_policy_config01_deviceinstallation02-class"></a><span data-ttu-id="bee6f-105">MDM \_ 原則 \_ Config01 \_ DeviceInstallation02 類別</span><span class="sxs-lookup"><span data-stu-id="bee6f-105">MDM\_Policy\_Config01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="bee6f-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bee6f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bee6f-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bee6f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bee6f-108">MDM \_ Policy \_ Config01 DeviceInstallation02 類別會設定 \_ 可用的裝置安裝原則。</span><span class="sxs-lookup"><span data-stu-id="bee6f-108">The MDM\_Policy\_Config01\_DeviceInstallation02 class configures the available device installation policies.</span></span>

<span data-ttu-id="bee6f-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bee6f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee6f-110">語法</span><span class="sxs-lookup"><span data-stu-id="bee6f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="bee6f-111">成員</span><span class="sxs-lookup"><span data-stu-id="bee6f-111">Members</span></span>

<span data-ttu-id="bee6f-112">**MDM \_ Policy \_ Config01 \_ DeviceInstallation02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bee6f-112">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="bee6f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bee6f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bee6f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bee6f-114">Properties</span></span>

<span data-ttu-id="bee6f-115">**MDM \_ Policy \_ Config01 \_ DeviceInstallation02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bee6f-115">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bee6f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bee6f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee6f-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bee6f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bee6f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bee6f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bee6f-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bee6f-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee6f-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bee6f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bee6f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bee6f-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bee6f-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="bee6f-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee6f-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bee6f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bee6f-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bee6f-127">PreventInstallationOfMatchingDeviceSetupClasses</span><span class="sxs-lookup"><span data-stu-id="bee6f-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee6f-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bee6f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee6f-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bee6f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bee6f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bee6f-130">Requirements</span></span>



| <span data-ttu-id="bee6f-131">需求</span><span class="sxs-lookup"><span data-stu-id="bee6f-131">Requirement</span></span> | <span data-ttu-id="bee6f-132">值</span><span class="sxs-lookup"><span data-stu-id="bee6f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee6f-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bee6f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bee6f-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bee6f-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bee6f-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bee6f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bee6f-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="bee6f-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bee6f-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="bee6f-137">Namespace</span></span><br/>                | <span data-ttu-id="bee6f-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bee6f-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bee6f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bee6f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bee6f-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="bee6f-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bee6f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bee6f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee6f-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee6f-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

