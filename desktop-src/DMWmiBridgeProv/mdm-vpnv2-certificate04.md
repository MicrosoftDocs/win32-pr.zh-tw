---
title: MDM_VPNv2_Certificate04 類別
description: 保留供日後使用。
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- MDM_VPNv2_Certificate04 類別
- MDM_VPNv2_Certificate04 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934390"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="8fd61-105">MDM \_ >vpnv2 \_ Certificate04 類別</span><span class="sxs-lookup"><span data-stu-id="8fd61-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="8fd61-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="8fd61-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8fd61-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="8fd61-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8fd61-108">保留供日後使用</span><span class="sxs-lookup"><span data-stu-id="8fd61-108">Reserved for future Use</span></span>

<span data-ttu-id="8fd61-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd61-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd61-110">語法</span><span class="sxs-lookup"><span data-stu-id="8fd61-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="8fd61-111">成員</span><span class="sxs-lookup"><span data-stu-id="8fd61-111">Members</span></span>

<span data-ttu-id="8fd61-112">**MDM \_ >vpnv2 \_ Certificate04** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8fd61-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="8fd61-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd61-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fd61-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd61-114">Properties</span></span>

<span data-ttu-id="8fd61-115">**MDM \_ >vpnv2 \_ Certificate04** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd61-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8fd61-116">Eku</span><span class="sxs-lookup"><span data-stu-id="8fd61-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd61-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd61-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8fd61-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8fd61-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8fd61-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd61-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd61-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd61-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fd61-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fd61-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fd61-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8fd61-124">針對此類別，字串為 "Eap"</span><span class="sxs-lookup"><span data-stu-id="8fd61-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="8fd61-125">Issuer</span><span class="sxs-lookup"><span data-stu-id="8fd61-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd61-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd61-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8fd61-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8fd61-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8fd61-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd61-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd61-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd61-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd61-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8fd61-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8fd61-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8fd61-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="8fd61-133">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="8fd61-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fd61-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fd61-134">Requirements</span></span>



| <span data-ttu-id="8fd61-135">需求</span><span class="sxs-lookup"><span data-stu-id="8fd61-135">Requirement</span></span> | <span data-ttu-id="8fd61-136">值</span><span class="sxs-lookup"><span data-stu-id="8fd61-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd61-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fd61-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd61-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fd61-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fd61-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fd61-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd61-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="8fd61-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8fd61-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fd61-141">Namespace</span></span><br/>                | <span data-ttu-id="8fd61-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8fd61-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8fd61-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8fd61-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fd61-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fd61-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fd61-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8fd61-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fd61-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fd61-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd61-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fd61-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd61-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="8fd61-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

