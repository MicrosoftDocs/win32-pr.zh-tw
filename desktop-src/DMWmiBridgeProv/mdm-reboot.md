---
title: MDM_Reboot 類別
description: MDM \_ Rebootclass 可用來設定重新開機設定。
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- MDM_Reboot 類別
- MDM_Reboot 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024632"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="d3ad4-105">MDM \_ 重新開機類別</span><span class="sxs-lookup"><span data-stu-id="d3ad4-105">MDM\_Reboot class</span></span>

<span data-ttu-id="d3ad4-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d3ad4-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d3ad4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d3ad4-108">**MDM \_ 重新開機** 類別是用來設定重新開機設定。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="d3ad4-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ad4-110">語法</span><span class="sxs-lookup"><span data-stu-id="d3ad4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="d3ad4-111">成員</span><span class="sxs-lookup"><span data-stu-id="d3ad4-111">Members</span></span>

<span data-ttu-id="d3ad4-112">**MDM \_ 重新開機** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3ad4-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="d3ad4-113">方法</span><span class="sxs-lookup"><span data-stu-id="d3ad4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3ad4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d3ad4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d3ad4-115">方法</span><span class="sxs-lookup"><span data-stu-id="d3ad4-115">Methods</span></span>

<span data-ttu-id="d3ad4-116">**MDM \_ 重新開機** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="d3ad4-117">方法</span><span class="sxs-lookup"><span data-stu-id="d3ad4-117">Method</span></span>                                                | <span data-ttu-id="d3ad4-118">描述</span><span class="sxs-lookup"><span data-stu-id="d3ad4-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="d3ad4-119">**RebootNowMethod**</span><span class="sxs-lookup"><span data-stu-id="d3ad4-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="d3ad4-120">此方法會執行裝置的重新開機。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d3ad4-121">屬性</span><span class="sxs-lookup"><span data-stu-id="d3ad4-121">Properties</span></span>

<span data-ttu-id="d3ad4-122">**MDM \_ 重新開機** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3ad4-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d3ad4-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ad4-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3ad4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3ad4-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ad4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ad4-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d3ad4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d3ad4-127">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="d3ad4-128">針對此類別，字串為「重新開機」。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="d3ad4-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d3ad4-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3ad4-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d3ad4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3ad4-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d3ad4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3ad4-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d3ad4-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d3ad4-133">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d3ad4-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="d3ad4-134">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="d3ad4-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3ad4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3ad4-135">Requirements</span></span>



| <span data-ttu-id="d3ad4-136">需求</span><span class="sxs-lookup"><span data-stu-id="d3ad4-136">Requirement</span></span> | <span data-ttu-id="d3ad4-137">值</span><span class="sxs-lookup"><span data-stu-id="d3ad4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ad4-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3ad4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ad4-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3ad4-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d3ad4-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3ad4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ad4-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="d3ad4-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d3ad4-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3ad4-142">Namespace</span></span><br/>                | <span data-ttu-id="d3ad4-143">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d3ad4-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d3ad4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d3ad4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3ad4-145"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad4-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="d3ad4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ad4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ad4-147"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad4-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

