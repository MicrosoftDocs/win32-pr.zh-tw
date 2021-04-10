---
title: MDM_Policy_Config01_Storage02 類別
description: MDM \_ Policy \_ Config01 Storage02 類別會設定 \_ 儲存體原則。
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- MDM_Policy_Config01_Storage02 類別
- MDM_Policy_Config01_Storage02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103895"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="f9e5a-105">MDM \_ 原則 \_ Config01 \_ Storage02 類別</span><span class="sxs-lookup"><span data-stu-id="f9e5a-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="f9e5a-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="f9e5a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f9e5a-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="f9e5a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f9e5a-108">MDM \_ Policy \_ Config01 Storage02 類別會設定 \_ 儲存體原則。</span><span class="sxs-lookup"><span data-stu-id="f9e5a-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="f9e5a-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9e5a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e5a-110">語法</span><span class="sxs-lookup"><span data-stu-id="f9e5a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="f9e5a-111">成員</span><span class="sxs-lookup"><span data-stu-id="f9e5a-111">Members</span></span>

<span data-ttu-id="f9e5a-112">**MDM \_ Policy \_ Config01 \_ Storage02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9e5a-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="f9e5a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f9e5a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9e5a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f9e5a-114">Properties</span></span>

<span data-ttu-id="f9e5a-115">**MDM \_ Policy \_ Config01 \_ Storage02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9e5a-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f9e5a-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="f9e5a-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e5a-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9e5a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f9e5a-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="f9e5a-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e5a-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f9e5a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9e5a-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e5a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9e5a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9e5a-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9e5a-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e5a-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9e5a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9e5a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9e5a-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9e5a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9e5a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9e5a-130">Requirements</span></span>



| <span data-ttu-id="f9e5a-131">需求</span><span class="sxs-lookup"><span data-stu-id="f9e5a-131">Requirement</span></span> | <span data-ttu-id="f9e5a-132">值</span><span class="sxs-lookup"><span data-stu-id="f9e5a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e5a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9e5a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e5a-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9e5a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9e5a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9e5a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e5a-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="f9e5a-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f9e5a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9e5a-137">Namespace</span></span><br/>                | <span data-ttu-id="f9e5a-138">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f9e5a-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f9e5a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f9e5a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9e5a-140"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9e5a-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9e5a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f9e5a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9e5a-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9e5a-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

