---
title: MDM_Policy_User_Config01_Settings02 類別
description: MDM \_ Policy \_ User \_ Config01 Settings02 類別會設定 \_ 工作列中的其他行事曆。
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- MDM_Policy_User_Config01_Settings02 類別
- MDM_Policy_User_Config01_Settings02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103865"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="37e9b-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ Settings02 類別</span><span class="sxs-lookup"><span data-stu-id="37e9b-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="37e9b-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="37e9b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37e9b-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="37e9b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37e9b-108">MDM \_ Policy \_ User \_ Config01 Settings02 類別會設定 \_ 工作列中的其他行事曆。</span><span class="sxs-lookup"><span data-stu-id="37e9b-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="37e9b-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="37e9b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e9b-110">語法</span><span class="sxs-lookup"><span data-stu-id="37e9b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="37e9b-111">成員</span><span class="sxs-lookup"><span data-stu-id="37e9b-111">Members</span></span>

<span data-ttu-id="37e9b-112">**MDM \_ Policy \_ User \_ Config01 \_ Settings02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37e9b-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="37e9b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="37e9b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37e9b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="37e9b-114">Properties</span></span>

<span data-ttu-id="37e9b-115">**MDM \_ Policy \_ User \_ Config01 \_ Settings02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="37e9b-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="37e9b-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="37e9b-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37e9b-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="37e9b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="37e9b-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="37e9b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37e9b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37e9b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37e9b-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37e9b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37e9b-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37e9b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37e9b-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37e9b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37e9b-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="37e9b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37e9b-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37e9b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37e9b-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37e9b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37e9b-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37e9b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37e9b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="37e9b-127">Requirements</span></span>



| <span data-ttu-id="37e9b-128">需求</span><span class="sxs-lookup"><span data-stu-id="37e9b-128">Requirement</span></span> | <span data-ttu-id="37e9b-129">值</span><span class="sxs-lookup"><span data-stu-id="37e9b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e9b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37e9b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="37e9b-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37e9b-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37e9b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37e9b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="37e9b-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="37e9b-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="37e9b-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="37e9b-134">Namespace</span></span><br/>                | <span data-ttu-id="37e9b-135">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="37e9b-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="37e9b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="37e9b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37e9b-137"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="37e9b-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37e9b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37e9b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37e9b-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37e9b-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

