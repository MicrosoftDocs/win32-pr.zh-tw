---
title: MDM_Firewall_Global02 類別
description: MDM \_ 防火牆 \_ Global02 類別可用來設定 Windows Defender 防火牆設定。
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- MDM_Firewall_Global02 類別
- MDM_Firewall_Global02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187280"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="33d2a-105">MDM \_ 防火牆 \_ Global02 類別</span><span class="sxs-lookup"><span data-stu-id="33d2a-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="33d2a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="33d2a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33d2a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="33d2a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33d2a-108">MDM \_ 防火牆 \_ Global02 類別可用來設定 Windows Defender 防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="33d2a-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="33d2a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="33d2a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d2a-110">語法</span><span class="sxs-lookup"><span data-stu-id="33d2a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="33d2a-111">成員</span><span class="sxs-lookup"><span data-stu-id="33d2a-111">Members</span></span>

<span data-ttu-id="33d2a-112">**MDM \_ 防火牆 \_ Global02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="33d2a-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="33d2a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="33d2a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33d2a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="33d2a-114">Properties</span></span>

<span data-ttu-id="33d2a-115">**MDM \_ 防火牆 \_ Global02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="33d2a-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33d2a-116">BinaryVersionSupported</span><span class="sxs-lookup"><span data-stu-id="33d2a-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33d2a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-119">CRLcheck</span><span class="sxs-lookup"><span data-stu-id="33d2a-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-122">CurrentProfiles</span><span class="sxs-lookup"><span data-stu-id="33d2a-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-125">DisableStatefulFtp</span><span class="sxs-lookup"><span data-stu-id="33d2a-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="33d2a-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-128">EnablePacketQueue</span><span class="sxs-lookup"><span data-stu-id="33d2a-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33d2a-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33d2a-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33d2a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="33d2a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33d2a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-135">IPsecExempt</span><span class="sxs-lookup"><span data-stu-id="33d2a-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-136">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-138">OpportunisticallyMatchAuthSetPerKM</span><span class="sxs-lookup"><span data-stu-id="33d2a-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="33d2a-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33d2a-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="33d2a-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33d2a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="33d2a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-144">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33d2a-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="33d2a-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33d2a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-148">PolicyVersionSupported</span><span class="sxs-lookup"><span data-stu-id="33d2a-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-149">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-151">PresharedKeyEncoding</span><span class="sxs-lookup"><span data-stu-id="33d2a-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-152">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33d2a-154">SaIdleTime</span><span class="sxs-lookup"><span data-stu-id="33d2a-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33d2a-155">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33d2a-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33d2a-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33d2a-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33d2a-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="33d2a-157">Requirements</span></span>



| <span data-ttu-id="33d2a-158">需求</span><span class="sxs-lookup"><span data-stu-id="33d2a-158">Requirement</span></span> | <span data-ttu-id="33d2a-159">值</span><span class="sxs-lookup"><span data-stu-id="33d2a-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d2a-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33d2a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="33d2a-161">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33d2a-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33d2a-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33d2a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="33d2a-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="33d2a-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="33d2a-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="33d2a-164">Namespace</span></span><br/>                | <span data-ttu-id="33d2a-165">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="33d2a-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="33d2a-166">MOF</span><span class="sxs-lookup"><span data-stu-id="33d2a-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33d2a-167"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="33d2a-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="33d2a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="33d2a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d2a-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33d2a-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

