---
title: MDM_PassportForWork_Remote03 類別
description: MDM \_ PassportForWork \_ Remote03 類別會定義 Windows Hello 企業版遠端原則設定。
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- MDM_PassportForWork_Remote03 類別
- MDM_PassportForWork_Remote03 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024912"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="103e4-105">MDM \_ PassportForWork \_ Remote03 類別</span><span class="sxs-lookup"><span data-stu-id="103e4-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="103e4-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="103e4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="103e4-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="103e4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="103e4-108">**MDM \_ PassportForWork \_ Remote03** 類別會定義 Windows Hello 企業版遠端原則設定。</span><span class="sxs-lookup"><span data-stu-id="103e4-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="103e4-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="103e4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="103e4-110">語法</span><span class="sxs-lookup"><span data-stu-id="103e4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="103e4-111">成員</span><span class="sxs-lookup"><span data-stu-id="103e4-111">Members</span></span>

<span data-ttu-id="103e4-112">**MDM \_ PassportForWork \_ Remote03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="103e4-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="103e4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="103e4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="103e4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="103e4-114">Properties</span></span>

<span data-ttu-id="103e4-115">**MDM \_ PassportForWork \_ Remote03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="103e4-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="103e4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="103e4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103e4-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103e4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103e4-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103e4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103e4-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103e4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="103e4-120">用來定義遠端 Windows Hello 企業版原則的內部節點。</span><span class="sxs-lookup"><span data-stu-id="103e4-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="103e4-121">此節點已加入 Windows 10 1511 版中。</span><span class="sxs-lookup"><span data-stu-id="103e4-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="103e4-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="103e4-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103e4-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103e4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103e4-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103e4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103e4-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103e4-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="103e4-126">用來定義 Windows Hello 企業版原則設定的節點。</span><span class="sxs-lookup"><span data-stu-id="103e4-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="103e4-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="103e4-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103e4-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="103e4-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="103e4-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103e4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="103e4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="103e4-130">Requirements</span></span>



| <span data-ttu-id="103e4-131">需求</span><span class="sxs-lookup"><span data-stu-id="103e4-131">Requirement</span></span> | <span data-ttu-id="103e4-132">值</span><span class="sxs-lookup"><span data-stu-id="103e4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103e4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="103e4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="103e4-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="103e4-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="103e4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="103e4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="103e4-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="103e4-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="103e4-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="103e4-137">Namespace</span></span><br/>                | <span data-ttu-id="103e4-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="103e4-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="103e4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="103e4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="103e4-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="103e4-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="103e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="103e4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="103e4-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103e4-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103e4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="103e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103e4-144">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="103e4-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

