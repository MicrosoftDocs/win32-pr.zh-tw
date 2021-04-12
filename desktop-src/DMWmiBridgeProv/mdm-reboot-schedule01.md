---
title: MDM_Reboot_Schedule01 類別
description: MDM \_ 重新開機 \_ Schedule01class 可用來設定裝置重新開機的特定時間。
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- MDM_Reboot_Schedule01 類別
- MDM_Reboot_Schedule01 類別，描述
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464357"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="4c5c0-105">MDM \_ 重新開機 \_ Schedule01 類別</span><span class="sxs-lookup"><span data-stu-id="4c5c0-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="4c5c0-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4c5c0-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="4c5c0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4c5c0-108">**MDM \_ 重新開機 \_ Schedule01** 類別可用來設定裝置重新開機的特定時間。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="4c5c0-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5c0-110">語法</span><span class="sxs-lookup"><span data-stu-id="4c5c0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="4c5c0-111">成員</span><span class="sxs-lookup"><span data-stu-id="4c5c0-111">Members</span></span>

<span data-ttu-id="4c5c0-112">**MDM \_ 重新開機 \_ Schedule01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4c5c0-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="4c5c0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4c5c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c5c0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4c5c0-114">Properties</span></span>

<span data-ttu-id="4c5c0-115">**MDM \_ 重新開機 \_ Schedule01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4c5c0-116">DailyRecurrent</span><span class="sxs-lookup"><span data-stu-id="4c5c0-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5c0-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4c5c0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4c5c0-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5c0-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c5c0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c5c0-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c5c0-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="4c5c0-124">此類別的字串為 "Schedule"。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="4c5c0-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5c0-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4c5c0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c5c0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c5c0-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4c5c0-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="4c5c0-130">此類別的字串為 "./Vendor/MSFT/Reboot"</span><span class="sxs-lookup"><span data-stu-id="4c5c0-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="4c5c0-131">Single</span><span class="sxs-lookup"><span data-stu-id="4c5c0-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5c0-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c5c0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c5c0-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4c5c0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c5c0-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c5c0-134">Requirements</span></span>



| <span data-ttu-id="4c5c0-135">需求</span><span class="sxs-lookup"><span data-stu-id="4c5c0-135">Requirement</span></span> | <span data-ttu-id="4c5c0-136">值</span><span class="sxs-lookup"><span data-stu-id="4c5c0-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5c0-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c5c0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5c0-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c5c0-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4c5c0-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c5c0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5c0-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="4c5c0-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4c5c0-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c5c0-141">Namespace</span></span><br/>                | <span data-ttu-id="4c5c0-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="4c5c0-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4c5c0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4c5c0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c5c0-144"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c5c0-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="4c5c0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5c0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5c0-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5c0-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

