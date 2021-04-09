---
title: MDM_Policy_Config01_Games02 類別
description: MDM \_ Policy \_ Config01 Games02 類別會設定 \_ advanced 遊戲服務。
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- MDM_Policy_Config01_Games02 類別
- MDM_Policy_Config01_Games02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025402"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="b3800-105">MDM \_ 原則 \_ Config01 \_ Games02 類別</span><span class="sxs-lookup"><span data-stu-id="b3800-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="b3800-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b3800-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3800-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b3800-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3800-108">MDM \_ Policy \_ Config01 Games02 類別會設定 \_ advanced 遊戲服務。</span><span class="sxs-lookup"><span data-stu-id="b3800-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="b3800-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3800-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3800-110">語法</span><span class="sxs-lookup"><span data-stu-id="b3800-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="b3800-111">成員</span><span class="sxs-lookup"><span data-stu-id="b3800-111">Members</span></span>

<span data-ttu-id="b3800-112">**MDM \_ Policy \_ Config01 \_ Games02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b3800-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="b3800-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b3800-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3800-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b3800-114">Properties</span></span>

<span data-ttu-id="b3800-115">**MDM \_ Policy \_ Config01 \_ Games02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b3800-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b3800-116">AllowAdvancedGamingServices</span><span class="sxs-lookup"><span data-stu-id="b3800-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3800-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3800-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3800-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b3800-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3800-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3800-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3800-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3800-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3800-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3800-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3800-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3800-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3800-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b3800-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3800-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3800-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3800-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3800-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3800-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3800-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3800-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3800-127">Requirements</span></span>



| <span data-ttu-id="b3800-128">需求</span><span class="sxs-lookup"><span data-stu-id="b3800-128">Requirement</span></span> | <span data-ttu-id="b3800-129">值</span><span class="sxs-lookup"><span data-stu-id="b3800-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3800-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3800-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3800-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3800-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3800-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3800-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3800-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3800-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b3800-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3800-134">Namespace</span></span><br/>                | <span data-ttu-id="b3800-135">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b3800-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b3800-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b3800-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3800-137"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3800-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3800-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b3800-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3800-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3800-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

