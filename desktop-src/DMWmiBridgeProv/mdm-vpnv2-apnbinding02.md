---
title: MDM_VPNv2_APNBinding02 類別
description: 保留供日後使用。 |MDM_VPNv2_APNBinding02 類別
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- MDM_VPNv2_APNBinding02 類別
- MDM_VPNv2_APNBinding02 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321936"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="a31ff-106">MDM \_ >vpnv2 \_ APNBinding02 類別</span><span class="sxs-lookup"><span data-stu-id="a31ff-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="a31ff-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a31ff-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a31ff-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a31ff-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a31ff-109">保留供日後使用</span><span class="sxs-lookup"><span data-stu-id="a31ff-109">Reserved for Future Use</span></span>

<span data-ttu-id="a31ff-110">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a31ff-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31ff-111">語法</span><span class="sxs-lookup"><span data-stu-id="a31ff-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="a31ff-112">成員</span><span class="sxs-lookup"><span data-stu-id="a31ff-112">Members</span></span>

<span data-ttu-id="a31ff-113">**MDM \_ >vpnv2 \_ APNBinding02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a31ff-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="a31ff-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a31ff-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a31ff-115">屬性</span><span class="sxs-lookup"><span data-stu-id="a31ff-115">Properties</span></span>

<span data-ttu-id="a31ff-116">**MDM \_ >vpnv2 \_ APNBinding02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a31ff-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a31ff-117">AccessPointName</span><span class="sxs-lookup"><span data-stu-id="a31ff-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a31ff-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a31ff-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a31ff-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a31ff-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a31ff-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a31ff-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a31ff-127">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a31ff-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="a31ff-128">IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="a31ff-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a31ff-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a31ff-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a31ff-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a31ff-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a31ff-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a31ff-135">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a31ff-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="a31ff-136">密碼</span><span class="sxs-lookup"><span data-stu-id="a31ff-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a31ff-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="a31ff-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a31ff-142">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a31ff-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a31ff-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a31ff-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a31ff-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a31ff-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a31ff-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31ff-145">Requirements</span></span>



| <span data-ttu-id="a31ff-146">需求</span><span class="sxs-lookup"><span data-stu-id="a31ff-146">Requirement</span></span> | <span data-ttu-id="a31ff-147">值</span><span class="sxs-lookup"><span data-stu-id="a31ff-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31ff-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31ff-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a31ff-149">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31ff-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a31ff-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31ff-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a31ff-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="a31ff-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a31ff-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="a31ff-152">Namespace</span></span><br/>                | <span data-ttu-id="a31ff-153">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a31ff-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a31ff-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a31ff-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a31ff-155"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a31ff-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a31ff-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a31ff-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a31ff-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a31ff-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a31ff-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a31ff-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31ff-159">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a31ff-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

