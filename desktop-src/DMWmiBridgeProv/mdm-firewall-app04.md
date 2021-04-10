---
title: MDM_Firewall_App04 類別
description: MDM \_ 防火牆 \_ App04 類別可用來設定 Windows Defender 防火牆設定。
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- MDM_Firewall_App04 類別
- MDM_Firewall_App04 類別，描述
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094284"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="8e79e-105">MDM \_ 防火牆 \_ App04 類別</span><span class="sxs-lookup"><span data-stu-id="8e79e-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="8e79e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="8e79e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8e79e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="8e79e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8e79e-108">MDM \_ 防火牆 \_ App04 類別可用來設定 Windows Defender 防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="8e79e-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="8e79e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e79e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e79e-110">語法</span><span class="sxs-lookup"><span data-stu-id="8e79e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="8e79e-111">成員</span><span class="sxs-lookup"><span data-stu-id="8e79e-111">Members</span></span>

<span data-ttu-id="8e79e-112">**MDM \_ 防火牆 \_ App04** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e79e-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="8e79e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8e79e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e79e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8e79e-114">Properties</span></span>

<span data-ttu-id="8e79e-115">**MDM \_ 防火牆 \_ App04** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e79e-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8e79e-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="8e79e-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e79e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8e79e-119">Fqbn</span><span class="sxs-lookup"><span data-stu-id="8e79e-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e79e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e79e-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8e79e-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e79e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e79e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8e79e-126">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="8e79e-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e79e-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e79e-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8e79e-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e79e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e79e-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8e79e-133">ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e79e-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e79e-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e79e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e79e-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e79e-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e79e-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e79e-136">Requirements</span></span>



| <span data-ttu-id="8e79e-137">需求</span><span class="sxs-lookup"><span data-stu-id="8e79e-137">Requirement</span></span> | <span data-ttu-id="8e79e-138">值</span><span class="sxs-lookup"><span data-stu-id="8e79e-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e79e-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e79e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8e79e-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e79e-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e79e-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e79e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8e79e-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="8e79e-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="8e79e-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e79e-143">Namespace</span></span><br/>                | <span data-ttu-id="8e79e-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8e79e-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="8e79e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8e79e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e79e-146"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e79e-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e79e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8e79e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e79e-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e79e-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

