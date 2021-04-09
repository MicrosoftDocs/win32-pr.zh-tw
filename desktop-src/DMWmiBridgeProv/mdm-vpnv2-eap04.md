---
title: MDM_VPNv2_Eap04 類別
description: '\_ \_ 當原生設定檔指定 EAP 驗證時，MDM >vpnv2 Eap04 類別包含必要的設定 XML 資訊。'
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- MDM_VPNv2_Eap04 類別
- MDM_VPNv2_Eap04 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686323"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="5913a-105">MDM \_ >vpnv2 \_ Eap04 類別</span><span class="sxs-lookup"><span data-stu-id="5913a-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="5913a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5913a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5913a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5913a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5913a-108">當原生設定檔指定 EAP 驗證時， **MDM \_ >vpnv2 \_ Eap04** 類別包含必要的設定 XML 資訊。</span><span class="sxs-lookup"><span data-stu-id="5913a-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="5913a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5913a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5913a-110">語法</span><span class="sxs-lookup"><span data-stu-id="5913a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="5913a-111">成員</span><span class="sxs-lookup"><span data-stu-id="5913a-111">Members</span></span>

<span data-ttu-id="5913a-112">**MDM \_ >vpnv2 \_ Eap04** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5913a-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="5913a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5913a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5913a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5913a-114">Properties</span></span>

<span data-ttu-id="5913a-115">**MDM \_ >vpnv2 \_ Eap04** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5913a-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5913a-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="5913a-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5913a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5913a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5913a-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5913a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5913a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5913a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5913a-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5913a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5913a-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5913a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5913a-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5913a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5913a-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5913a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="5913a-124">針對此類別，字串為 "Eap"</span><span class="sxs-lookup"><span data-stu-id="5913a-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="5913a-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5913a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5913a-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5913a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5913a-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5913a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5913a-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5913a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5913a-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5913a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="5913a-130">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="5913a-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="5913a-131">型別</span><span class="sxs-lookup"><span data-stu-id="5913a-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5913a-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5913a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5913a-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5913a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5913a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="5913a-134">Requirements</span></span>



| <span data-ttu-id="5913a-135">需求</span><span class="sxs-lookup"><span data-stu-id="5913a-135">Requirement</span></span> | <span data-ttu-id="5913a-136">值</span><span class="sxs-lookup"><span data-stu-id="5913a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5913a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5913a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5913a-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5913a-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5913a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5913a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5913a-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="5913a-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5913a-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="5913a-141">Namespace</span></span><br/>                | <span data-ttu-id="5913a-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="5913a-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5913a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5913a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5913a-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="5913a-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5913a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5913a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5913a-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5913a-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5913a-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5913a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5913a-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="5913a-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

