---
title: MDM_Policy_Config01_WirelessDisplay02 類別
description: MDM \_ Policy \_ Config01 \_ WirelessDisplay02 類別代表可用的無線顯示原則。
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- MDM_Policy_Config01_WirelessDisplay02 類別
- MDM_Policy_Config01_WirelessDisplay02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934440"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a><span data-ttu-id="01f58-105">MDM \_ 原則 \_ Config01 \_ WirelessDisplay02 類別</span><span class="sxs-lookup"><span data-stu-id="01f58-105">MDM\_Policy\_Config01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="01f58-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="01f58-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01f58-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="01f58-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01f58-108">**MDM \_ Policy \_ Config01 \_ WirelessDisplay02** 類別代表可用的無線顯示原則。</span><span class="sxs-lookup"><span data-stu-id="01f58-108">The **MDM\_Policy\_Config01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="01f58-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="01f58-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f58-110">語法</span><span class="sxs-lookup"><span data-stu-id="01f58-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="01f58-111">成員</span><span class="sxs-lookup"><span data-stu-id="01f58-111">Members</span></span>

<span data-ttu-id="01f58-112">**MDM \_ Policy \_ Config01 \_ WirelessDisplay02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01f58-112">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="01f58-113">屬性</span><span class="sxs-lookup"><span data-stu-id="01f58-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01f58-114">屬性</span><span class="sxs-lookup"><span data-stu-id="01f58-114">Properties</span></span>

<span data-ttu-id="01f58-115">**MDM \_ Policy \_ Config01 \_ WirelessDisplay02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01f58-115">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="01f58-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="01f58-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="01f58-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="01f58-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="01f58-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="01f58-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="01f58-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01f58-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="01f58-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01f58-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01f58-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f58-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f58-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f58-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01f58-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01f58-141">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="01f58-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="01f58-142">此類別的字串為 "WirelessDisplay"。</span><span class="sxs-lookup"><span data-stu-id="01f58-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="01f58-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="01f58-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01f58-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01f58-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01f58-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01f58-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01f58-147">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="01f58-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="01f58-148">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="01f58-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="01f58-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="01f58-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01f58-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="01f58-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="01f58-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="01f58-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01f58-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="01f58-152">Requirements</span></span>



| <span data-ttu-id="01f58-153">需求</span><span class="sxs-lookup"><span data-stu-id="01f58-153">Requirement</span></span> | <span data-ttu-id="01f58-154">值</span><span class="sxs-lookup"><span data-stu-id="01f58-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f58-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01f58-155">Minimum supported client</span></span><br/> | <span data-ttu-id="01f58-156">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f58-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="01f58-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01f58-157">Minimum supported server</span></span><br/> | <span data-ttu-id="01f58-158">都不支援</span><span class="sxs-lookup"><span data-stu-id="01f58-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="01f58-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="01f58-159">Namespace</span></span><br/>                | <span data-ttu-id="01f58-160">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="01f58-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="01f58-161">MOF</span><span class="sxs-lookup"><span data-stu-id="01f58-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f58-162"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f58-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="01f58-163">DLL</span><span class="sxs-lookup"><span data-stu-id="01f58-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f58-164"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f58-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

