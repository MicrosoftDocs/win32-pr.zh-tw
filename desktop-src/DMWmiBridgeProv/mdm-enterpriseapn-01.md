---
title: MDM_EnterpriseAPN_01 類別
description: '\_ \_ 企業會使用 MDM EnterpriseAPN 01 類別來布建網際網路的 APN。'
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- MDM_EnterpriseAPN_01 類別
- MDM_EnterpriseAPN_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187294"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="658e0-105">MDM \_ EnterpriseAPN \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="658e0-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="658e0-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="658e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="658e0-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="658e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="658e0-108">企業會使用 **MDM \_ EnterpriseAPN \_ 01** 類別來布建網際網路的 APN。</span><span class="sxs-lookup"><span data-stu-id="658e0-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="658e0-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="658e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="658e0-110">語法</span><span class="sxs-lookup"><span data-stu-id="658e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="658e0-111">成員</span><span class="sxs-lookup"><span data-stu-id="658e0-111">Members</span></span>

<span data-ttu-id="658e0-112">**MDM \_ EnterpriseAPN \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="658e0-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="658e0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="658e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="658e0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="658e0-114">Properties</span></span>

<span data-ttu-id="658e0-115">**MDM \_ EnterpriseAPN \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="658e0-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="658e0-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="658e0-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658e0-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-119">APNName</span><span class="sxs-lookup"><span data-stu-id="658e0-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="658e0-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-125">ClassId</span><span class="sxs-lookup"><span data-stu-id="658e0-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="658e0-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658e0-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-131">IccId</span><span class="sxs-lookup"><span data-stu-id="658e0-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="658e0-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="658e0-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658e0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658e0-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="658e0-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="658e0-138">Windows 連線管理員所見的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="658e0-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="658e0-139">IPType</span><span class="sxs-lookup"><span data-stu-id="658e0-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="658e0-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="658e0-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="658e0-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="658e0-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="658e0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658e0-148">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="658e0-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="658e0-149">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="658e0-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="658e0-150">此類別的字串為 "./Vendor/MSFT/EnterpriseAPN"</span><span class="sxs-lookup"><span data-stu-id="658e0-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="658e0-151">密碼</span><span class="sxs-lookup"><span data-stu-id="658e0-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-154">漫遊</span><span class="sxs-lookup"><span data-stu-id="658e0-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="658e0-157">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="658e0-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="658e0-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="658e0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658e0-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="658e0-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="658e0-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="658e0-160">Requirements</span></span>



| <span data-ttu-id="658e0-161">需求</span><span class="sxs-lookup"><span data-stu-id="658e0-161">Requirement</span></span> | <span data-ttu-id="658e0-162">值</span><span class="sxs-lookup"><span data-stu-id="658e0-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="658e0-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="658e0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="658e0-164">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="658e0-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="658e0-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="658e0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="658e0-166">都不支援</span><span class="sxs-lookup"><span data-stu-id="658e0-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="658e0-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="658e0-167">Namespace</span></span><br/>                | <span data-ttu-id="658e0-168">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="658e0-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="658e0-169">MOF</span><span class="sxs-lookup"><span data-stu-id="658e0-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="658e0-170"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="658e0-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="658e0-171">DLL</span><span class="sxs-lookup"><span data-stu-id="658e0-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="658e0-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="658e0-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658e0-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="658e0-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658e0-174">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="658e0-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

