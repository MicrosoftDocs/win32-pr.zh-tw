---
title: MDM_PassportForWork 類別
description: MDM \_ PassportForWork 可用來布建 Windows Hello 企業版。
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- MDM_PassportForWork 類別
- MDM_PassportForWork 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024911"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="d044a-105">MDM \_ PassportForWork 類別</span><span class="sxs-lookup"><span data-stu-id="d044a-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="d044a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d044a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d044a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d044a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d044a-108">**MDM \_ PassportForWork** 可用來布建 Windows Hello 企業版。</span><span class="sxs-lookup"><span data-stu-id="d044a-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="d044a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d044a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d044a-110">語法</span><span class="sxs-lookup"><span data-stu-id="d044a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="d044a-111">成員</span><span class="sxs-lookup"><span data-stu-id="d044a-111">Members</span></span>

<span data-ttu-id="d044a-112">**MDM \_ PassportForWork** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d044a-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="d044a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d044a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d044a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d044a-114">Properties</span></span>

<span data-ttu-id="d044a-115">**MDM \_ PassportForWork** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d044a-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d044a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d044a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d044a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d044a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d044a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d044a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d044a-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d044a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d044a-120">以全域唯一識別碼的格式指定租使用者識別碼 (GUID) 沒有大括弧 ( {，} ) ，它將作為 Windows Hello 企業版布建和管理的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="d044a-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="d044a-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d044a-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d044a-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d044a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d044a-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d044a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d044a-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d044a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d044a-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d044a-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d044a-126">此類別的字串為 "./Vendor/MSFT/PassPortForWork/"</span><span class="sxs-lookup"><span data-stu-id="d044a-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="d044a-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="d044a-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d044a-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d044a-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d044a-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d044a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d044a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d044a-130">Requirements</span></span>



| <span data-ttu-id="d044a-131">需求</span><span class="sxs-lookup"><span data-stu-id="d044a-131">Requirement</span></span> | <span data-ttu-id="d044a-132">值</span><span class="sxs-lookup"><span data-stu-id="d044a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d044a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d044a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d044a-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d044a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d044a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d044a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d044a-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="d044a-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d044a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="d044a-137">Namespace</span></span><br/>                | <span data-ttu-id="d044a-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d044a-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d044a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d044a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d044a-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d044a-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d044a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d044a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d044a-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d044a-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d044a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d044a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d044a-144">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="d044a-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

