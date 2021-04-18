---
title: MDM_Policy_User_Config01_Notifications02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ Notifications02 類別代表可用的通知原則。
ms.assetid: da70b3b4-e8ed-4784-ad6b-52e152a8b78f
keywords:
- MDM_Policy_User_Config01_Notifications02 類別
- MDM_Policy_User_Config01_Notifications02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02.InstanceID
- MDM_Policy_User_Config01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c85dcd9a622d29baf6d7c8f28d9e72b68998ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103872"
---
# <a name="mdm_policy_user_config01_notifications02-class"></a><span data-ttu-id="11e72-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ Notifications02 類別</span><span class="sxs-lookup"><span data-stu-id="11e72-105">MDM\_Policy\_User\_Config01\_Notifications02 class</span></span>

<span data-ttu-id="11e72-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="11e72-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11e72-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="11e72-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11e72-108">**MDM \_ Policy \_ User \_ Config01 \_ Notifications02** 類別代表可用的通知原則。</span><span class="sxs-lookup"><span data-stu-id="11e72-108">The **MDM\_Policy\_User\_Config01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="11e72-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="11e72-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e72-110">語法</span><span class="sxs-lookup"><span data-stu-id="11e72-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="11e72-111">成員</span><span class="sxs-lookup"><span data-stu-id="11e72-111">Members</span></span>

<span data-ttu-id="11e72-112">**MDM \_ Policy \_ User \_ Config01 \_ Notifications02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11e72-112">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="11e72-113">屬性</span><span class="sxs-lookup"><span data-stu-id="11e72-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11e72-114">屬性</span><span class="sxs-lookup"><span data-stu-id="11e72-114">Properties</span></span>

<span data-ttu-id="11e72-115">**MDM \_ Policy \_ User \_ Config01 \_ Notifications02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="11e72-115">The **MDM\_Policy\_User\_Config01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11e72-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="11e72-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e72-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="11e72-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11e72-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="11e72-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11e72-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11e72-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e72-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11e72-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11e72-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11e72-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11e72-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11e72-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11e72-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e72-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="11e72-124">針對此類別，字串為「通知」。</span><span class="sxs-lookup"><span data-stu-id="11e72-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="11e72-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11e72-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11e72-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11e72-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11e72-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11e72-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11e72-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11e72-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11e72-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="11e72-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="11e72-130">此類別的字串為 "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="11e72-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11e72-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="11e72-131">Requirements</span></span>



| <span data-ttu-id="11e72-132">需求</span><span class="sxs-lookup"><span data-stu-id="11e72-132">Requirement</span></span> | <span data-ttu-id="11e72-133">值</span><span class="sxs-lookup"><span data-stu-id="11e72-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e72-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11e72-134">Minimum supported client</span></span><br/> | <span data-ttu-id="11e72-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11e72-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="11e72-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11e72-136">Minimum supported server</span></span><br/> | <span data-ttu-id="11e72-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="11e72-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="11e72-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="11e72-138">Namespace</span></span><br/>                | <span data-ttu-id="11e72-139">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="11e72-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="11e72-140">MOF</span><span class="sxs-lookup"><span data-stu-id="11e72-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11e72-141"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="11e72-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="11e72-142">DLL</span><span class="sxs-lookup"><span data-stu-id="11e72-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e72-143"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e72-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

