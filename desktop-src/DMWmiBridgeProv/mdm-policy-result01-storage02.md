---
title: MDM_Policy_Result01_Storage02 類別
description: MDM \_ Policy \_ Result01 \_ Storage02 類別代表可用的儲存體原則。
ms.assetid: e0e3b867-38b5-4b10-a13e-6f99b8ff6db3
keywords:
- MDM_Policy_Result01_Storage02 類別
- MDM_Policy_Result01_Storage02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Storage02
- MDM_Policy_Result01_Storage02.InstanceID
- MDM_Policy_Result01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63381b34c88ebc590577eec9a11f603ea5325649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024975"
---
# <a name="mdm_policy_result01_storage02-class"></a><span data-ttu-id="db5bf-105">MDM \_ 原則 \_ Result01 \_ Storage02 類別</span><span class="sxs-lookup"><span data-stu-id="db5bf-105">MDM\_Policy\_Result01\_Storage02 class</span></span>

<span data-ttu-id="db5bf-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="db5bf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db5bf-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="db5bf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db5bf-108">MDM \_ Policy \_ Result01 \_ Storage02 類別代表可用的儲存體原則。</span><span class="sxs-lookup"><span data-stu-id="db5bf-108">The MDM\_Policy\_Result01\_Storage02 class represents the available storage policies.</span></span>

<span data-ttu-id="db5bf-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="db5bf-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5bf-110">語法</span><span class="sxs-lookup"><span data-stu-id="db5bf-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="db5bf-111">成員</span><span class="sxs-lookup"><span data-stu-id="db5bf-111">Members</span></span>

<span data-ttu-id="db5bf-112">**MDM \_ Policy \_ Result01 \_ Storage02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="db5bf-112">The **MDM\_Policy\_Result01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="db5bf-113">屬性</span><span class="sxs-lookup"><span data-stu-id="db5bf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db5bf-114">屬性</span><span class="sxs-lookup"><span data-stu-id="db5bf-114">Properties</span></span>

<span data-ttu-id="db5bf-115">**MDM \_ Policy \_ Result01 \_ Storage02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="db5bf-115">The **MDM\_Policy\_Result01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="db5bf-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="db5bf-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5bf-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="db5bf-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="db5bf-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db5bf-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="db5bf-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5bf-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db5bf-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="db5bf-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db5bf-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="db5bf-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5bf-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db5bf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db5bf-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db5bf-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db5bf-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="db5bf-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db5bf-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="db5bf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="db5bf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db5bf-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db5bf-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db5bf-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="db5bf-130">Requirements</span></span>



| <span data-ttu-id="db5bf-131">需求</span><span class="sxs-lookup"><span data-stu-id="db5bf-131">Requirement</span></span> | <span data-ttu-id="db5bf-132">值</span><span class="sxs-lookup"><span data-stu-id="db5bf-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db5bf-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db5bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="db5bf-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db5bf-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db5bf-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db5bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="db5bf-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="db5bf-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="db5bf-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="db5bf-137">Namespace</span></span><br/>                | <span data-ttu-id="db5bf-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="db5bf-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="db5bf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="db5bf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db5bf-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="db5bf-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="db5bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="db5bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db5bf-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5bf-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

