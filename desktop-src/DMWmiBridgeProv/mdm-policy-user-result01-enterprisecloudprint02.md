---
title: MDM_Policy_User_Result01_EnterpriseCloudPrint02 類別
description: MDM \_ Policy \_ User \_ Result01 \_ EnterpriseCloudPrint02 類別代表可用的雲端列印原則。
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02 類別
- MDM_Policy_User_Result01_EnterpriseCloudPrint02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dfa75d102da3a61ff0a9f2094d31e0ba5b4abca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465421"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a><span data-ttu-id="e0369-105">MDM \_ 原則 \_ 使用者 \_ Result01 \_ EnterpriseCloudPrint02 類別</span><span class="sxs-lookup"><span data-stu-id="e0369-105">MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="e0369-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e0369-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e0369-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e0369-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e0369-108">MDM \_ Policy \_ User \_ Result01 \_ EnterpriseCloudPrint02 類別代表可用的雲端列印原則。</span><span class="sxs-lookup"><span data-stu-id="e0369-108">The MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="e0369-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0369-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0369-110">語法</span><span class="sxs-lookup"><span data-stu-id="e0369-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="e0369-111">成員</span><span class="sxs-lookup"><span data-stu-id="e0369-111">Members</span></span>

<span data-ttu-id="e0369-112">**MDM \_ Policy \_ User \_ Result01 \_ EnterpriseCloudPrint02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0369-112">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="e0369-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e0369-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0369-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e0369-114">Properties</span></span>

<span data-ttu-id="e0369-115">**MDM \_ Policy \_ User \_ Result01 \_ EnterpriseCloudPrint02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e0369-115">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e0369-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="e0369-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0369-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="e0369-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0369-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="e0369-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0369-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="e0369-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0369-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="e0369-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0369-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0369-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e0369-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0369-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0369-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0369-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e0369-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="e0369-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e0369-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0369-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e0369-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0369-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0369-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0369-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0369-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0369-141">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e0369-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0369-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0369-142">Requirements</span></span>



| <span data-ttu-id="e0369-143">需求</span><span class="sxs-lookup"><span data-stu-id="e0369-143">Requirement</span></span> | <span data-ttu-id="e0369-144">值</span><span class="sxs-lookup"><span data-stu-id="e0369-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0369-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0369-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e0369-146">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0369-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0369-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0369-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e0369-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="e0369-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e0369-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="e0369-149">Namespace</span></span><br/>                | <span data-ttu-id="e0369-150">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e0369-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e0369-151">MOF</span><span class="sxs-lookup"><span data-stu-id="e0369-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0369-152"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0369-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0369-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e0369-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0369-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0369-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

