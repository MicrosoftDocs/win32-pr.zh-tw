---
title: MDM_Policy_Config01_EventLogService02 類別
description: MDM \_ Policy \_ Config01 EventLogService02 類別會設定 \_ 事件記錄檔的行為。
ms.assetid: 206934c4-6671-4f13-be79-22ff1fb7ce7e
keywords:
- MDM_Policy_Config01_EventLogService02 類別
- MDM_Policy_Config01_EventLogService02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_EventLogService02
- MDM_Policy_Config01_EventLogService02.InstanceID
- MDM_Policy_Config01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e39d3e78e686886e689ab2333b073108207446a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934179"
---
# <a name="mdm_policy_config01_eventlogservice02-class"></a><span data-ttu-id="8ba91-105">MDM \_ 原則 \_ Config01 \_ EventLogService02 類別</span><span class="sxs-lookup"><span data-stu-id="8ba91-105">MDM\_Policy\_Config01\_EventLogService02 class</span></span>

<span data-ttu-id="8ba91-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="8ba91-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ba91-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="8ba91-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ba91-108">MDM \_ Policy \_ Config01 EventLogService02 類別會設定 \_ 事件記錄檔的行為。</span><span class="sxs-lookup"><span data-stu-id="8ba91-108">The MDM\_Policy\_Config01\_EventLogService02 class configures the event log behavior.</span></span>

<span data-ttu-id="8ba91-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8ba91-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba91-110">語法</span><span class="sxs-lookup"><span data-stu-id="8ba91-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="8ba91-111">成員</span><span class="sxs-lookup"><span data-stu-id="8ba91-111">Members</span></span>

<span data-ttu-id="8ba91-112">**MDM \_ Policy \_ Config01 \_ EventLogService02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8ba91-112">The **MDM\_Policy\_Config01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="8ba91-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8ba91-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ba91-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8ba91-114">Properties</span></span>

<span data-ttu-id="8ba91-115">**MDM \_ Policy \_ Config01 \_ EventLogService02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8ba91-115">The **MDM\_Policy\_Config01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8ba91-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="8ba91-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ba91-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ba91-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ba91-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ba91-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ba91-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ba91-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8ba91-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ba91-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ba91-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ba91-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="8ba91-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ba91-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ba91-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="8ba91-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ba91-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ba91-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="8ba91-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ba91-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ba91-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ba91-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ba91-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ba91-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ba91-136">Requirements</span></span>



| <span data-ttu-id="8ba91-137">需求</span><span class="sxs-lookup"><span data-stu-id="8ba91-137">Requirement</span></span> | <span data-ttu-id="8ba91-138">值</span><span class="sxs-lookup"><span data-stu-id="8ba91-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba91-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ba91-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba91-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ba91-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ba91-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ba91-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba91-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="8ba91-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8ba91-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ba91-143">Namespace</span></span><br/>                | <span data-ttu-id="8ba91-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8ba91-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8ba91-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8ba91-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ba91-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ba91-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ba91-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8ba91-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba91-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba91-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

