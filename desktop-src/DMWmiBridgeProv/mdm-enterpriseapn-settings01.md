---
title: MDM_EnterpriseAPN_Settings01 類別
description: '\_ \_ 企業會使用 MDM EnterpriseAPN Settings01 類別來變更 APN 全域設定。'
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- MDM_EnterpriseAPN_Settings01 類別
- MDM_EnterpriseAPN_Settings01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104993"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="acddc-105">MDM \_ EnterpriseAPN \_ Settings01 類別</span><span class="sxs-lookup"><span data-stu-id="acddc-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="acddc-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="acddc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="acddc-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="acddc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="acddc-108">企業會使用 **MDM \_ EnterpriseAPN \_ Settings01** 類別來變更 APN 全域設定。</span><span class="sxs-lookup"><span data-stu-id="acddc-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="acddc-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="acddc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="acddc-110">語法</span><span class="sxs-lookup"><span data-stu-id="acddc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="acddc-111">成員</span><span class="sxs-lookup"><span data-stu-id="acddc-111">Members</span></span>

<span data-ttu-id="acddc-112">**MDM \_ EnterpriseAPN \_ Settings01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="acddc-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="acddc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="acddc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acddc-114">屬性</span><span class="sxs-lookup"><span data-stu-id="acddc-114">Properties</span></span>

<span data-ttu-id="acddc-115">**MDM \_ EnterpriseAPN \_ Settings01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="acddc-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="acddc-116">AllowUserControl</span><span class="sxs-lookup"><span data-stu-id="acddc-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="acddc-117">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="acddc-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="acddc-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acddc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="acddc-119">HideView</span><span class="sxs-lookup"><span data-stu-id="acddc-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="acddc-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="acddc-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="acddc-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acddc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="acddc-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="acddc-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acddc-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="acddc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acddc-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="acddc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acddc-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="acddc-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="acddc-126">包含 APN 全域設定的節點。</span><span class="sxs-lookup"><span data-stu-id="acddc-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="acddc-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="acddc-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acddc-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="acddc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acddc-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="acddc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acddc-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="acddc-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="acddc-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="acddc-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="acddc-132">此類別的字串為 "./Vendor/MSFT/EnterpriseAPN/Settings"</span><span class="sxs-lookup"><span data-stu-id="acddc-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acddc-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="acddc-133">Requirements</span></span>



| <span data-ttu-id="acddc-134">需求</span><span class="sxs-lookup"><span data-stu-id="acddc-134">Requirement</span></span> | <span data-ttu-id="acddc-135">值</span><span class="sxs-lookup"><span data-stu-id="acddc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acddc-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acddc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="acddc-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acddc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="acddc-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acddc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="acddc-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="acddc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="acddc-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="acddc-140">Namespace</span></span><br/>                | <span data-ttu-id="acddc-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="acddc-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="acddc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="acddc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acddc-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="acddc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="acddc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="acddc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acddc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acddc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

