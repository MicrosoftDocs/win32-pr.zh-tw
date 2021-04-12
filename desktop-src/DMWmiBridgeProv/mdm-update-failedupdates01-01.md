---
title: MDM_Update_FailedUpdates01_01 類別
description: MDM \_ Update \_ FailedUpdates01 \_ 01 類別可用來管理失敗的更新。
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- MDM_Update_FailedUpdates01_01 類別
- MDM_Update_FailedUpdates01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464345"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="fa059-105">MDM \_ Update \_ FailedUpdates01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="fa059-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="fa059-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fa059-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fa059-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fa059-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fa059-108">**MDM \_ Update \_ FailedUpdates01 \_ 01** 類別可用來管理失敗的更新。</span><span class="sxs-lookup"><span data-stu-id="fa059-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="fa059-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa059-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa059-110">語法</span><span class="sxs-lookup"><span data-stu-id="fa059-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="fa059-111">成員</span><span class="sxs-lookup"><span data-stu-id="fa059-111">Members</span></span>

<span data-ttu-id="fa059-112">**MDM \_ Update \_ FailedUpdates01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa059-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="fa059-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fa059-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa059-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fa059-114">Properties</span></span>

<span data-ttu-id="fa059-115">**MDM \_ Update \_ FailedUpdates01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa059-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fa059-116">HResult</span><span class="sxs-lookup"><span data-stu-id="fa059-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa059-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa059-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa059-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa059-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa059-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa059-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa059-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa059-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa059-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa059-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa059-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa059-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa059-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa059-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fa059-124">針對這個類別，字串是失敗更新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fa059-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="fa059-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fa059-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa059-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa059-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa059-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa059-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa059-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa059-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa059-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fa059-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fa059-130">此類別的字串為 "./Vendor/MSFT/Update/FailedUpdates"</span><span class="sxs-lookup"><span data-stu-id="fa059-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="fa059-131">**狀態**</span><span class="sxs-lookup"><span data-stu-id="fa059-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa059-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa059-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa059-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa059-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa059-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa059-134">Requirements</span></span>



| <span data-ttu-id="fa059-135">需求</span><span class="sxs-lookup"><span data-stu-id="fa059-135">Requirement</span></span> | <span data-ttu-id="fa059-136">值</span><span class="sxs-lookup"><span data-stu-id="fa059-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa059-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa059-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fa059-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa059-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fa059-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa059-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fa059-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa059-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fa059-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa059-141">Namespace</span></span><br/>                | <span data-ttu-id="fa059-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fa059-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fa059-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fa059-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa059-144"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa059-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="fa059-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fa059-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa059-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa059-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

