---
title: MDM_Policy_Config01_Maps02 類別
description: MDM \_ Policy \_ Config01 \_ Maps02 類別表示可用的對應原則。
ms.assetid: d2965f1f-a858-4b43-9c46-17ba718291b1
keywords:
- MDM_Policy_Config01_Maps02 類別
- MDM_Policy_Config01_Maps02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Maps02
- MDM_Policy_Config01_Maps02.InstanceID
- MDM_Policy_Config01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090c8d077b3df4446054d29a8100a32923932736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094567"
---
# <a name="mdm_policy_config01_maps02-class"></a><span data-ttu-id="26a01-105">MDM \_ 原則 \_ Config01 \_ Maps02 類別</span><span class="sxs-lookup"><span data-stu-id="26a01-105">MDM\_Policy\_Config01\_Maps02 class</span></span>

<span data-ttu-id="26a01-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="26a01-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26a01-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="26a01-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26a01-108">**MDM \_ Policy \_ Config01 \_ Maps02** 類別表示可用的對應原則。</span><span class="sxs-lookup"><span data-stu-id="26a01-108">The **MDM\_Policy\_Config01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="26a01-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="26a01-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a01-110">語法</span><span class="sxs-lookup"><span data-stu-id="26a01-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="26a01-111">成員</span><span class="sxs-lookup"><span data-stu-id="26a01-111">Members</span></span>

<span data-ttu-id="26a01-112">**MDM \_ Policy \_ Config01 \_ Maps02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26a01-112">The **MDM\_Policy\_Config01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="26a01-113">屬性</span><span class="sxs-lookup"><span data-stu-id="26a01-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26a01-114">屬性</span><span class="sxs-lookup"><span data-stu-id="26a01-114">Properties</span></span>

<span data-ttu-id="26a01-115">**MDM \_ Policy \_ Config01 \_ Maps02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="26a01-115">The **MDM\_Policy\_Config01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="26a01-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="26a01-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a01-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="26a01-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26a01-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="26a01-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26a01-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="26a01-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a01-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="26a01-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26a01-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="26a01-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26a01-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26a01-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a01-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a01-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a01-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a01-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26a01-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26a01-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26a01-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="26a01-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="26a01-127">此類別的字串為 "Map"。</span><span class="sxs-lookup"><span data-stu-id="26a01-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="26a01-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26a01-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a01-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a01-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a01-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a01-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26a01-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26a01-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26a01-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="26a01-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="26a01-133">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="26a01-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26a01-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="26a01-134">Requirements</span></span>



| <span data-ttu-id="26a01-135">需求</span><span class="sxs-lookup"><span data-stu-id="26a01-135">Requirement</span></span> | <span data-ttu-id="26a01-136">值</span><span class="sxs-lookup"><span data-stu-id="26a01-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a01-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26a01-137">Minimum supported client</span></span><br/> | <span data-ttu-id="26a01-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26a01-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="26a01-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26a01-139">Minimum supported server</span></span><br/> | <span data-ttu-id="26a01-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="26a01-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="26a01-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="26a01-141">Namespace</span></span><br/>                | <span data-ttu-id="26a01-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="26a01-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="26a01-143">MOF</span><span class="sxs-lookup"><span data-stu-id="26a01-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26a01-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="26a01-145">DLL</span><span class="sxs-lookup"><span data-stu-id="26a01-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a01-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

