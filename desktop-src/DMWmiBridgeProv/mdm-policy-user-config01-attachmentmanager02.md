---
title: MDM_Policy_User_Config01_AttachmentManager02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ AttachmentManager02 類別代表可用的附件管理員原則。
ms.assetid: b20ec516-cdc9-4aeb-802d-97cd8423eceb
keywords:
- MDM_Policy_User_Config01_AttachmentManager02 類別
- MDM_Policy_User_Config01_AttachmentManager02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_AttachmentManager02
- MDM_Policy_User_Config01_AttachmentManager02.InstanceID
- MDM_Policy_User_Config01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127fc3770f6ba605bd8e1efdd82314231ab27f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509011"
---
# <a name="mdm_policy_user_config01_attachmentmanager02-class"></a><span data-ttu-id="6062b-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ AttachmentManager02 類別</span><span class="sxs-lookup"><span data-stu-id="6062b-105">MDM\_Policy\_User\_Config01\_AttachmentManager02 class</span></span>

<span data-ttu-id="6062b-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6062b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6062b-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6062b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6062b-108">MDM \_ Policy \_ User \_ Config01 \_ AttachmentManager02 類別代表可用的附件管理員原則。</span><span class="sxs-lookup"><span data-stu-id="6062b-108">The MDM\_Policy\_User\_Config01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="6062b-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6062b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6062b-110">語法</span><span class="sxs-lookup"><span data-stu-id="6062b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="6062b-111">成員</span><span class="sxs-lookup"><span data-stu-id="6062b-111">Members</span></span>

<span data-ttu-id="6062b-112">**MDM \_ Policy \_ User \_ Config01 \_ AttachmentManager02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6062b-112">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="6062b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6062b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6062b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="6062b-114">Properties</span></span>

<span data-ttu-id="6062b-115">**MDM \_ Policy \_ User \_ Config01 \_ AttachmentManager02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6062b-115">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6062b-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="6062b-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6062b-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6062b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6062b-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6062b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6062b-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="6062b-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6062b-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6062b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6062b-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6062b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6062b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6062b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6062b-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6062b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6062b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6062b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6062b-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6062b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6062b-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="6062b-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6062b-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6062b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6062b-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6062b-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6062b-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6062b-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6062b-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6062b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6062b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6062b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6062b-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6062b-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6062b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6062b-133">Requirements</span></span>



| <span data-ttu-id="6062b-134">需求</span><span class="sxs-lookup"><span data-stu-id="6062b-134">Requirement</span></span> | <span data-ttu-id="6062b-135">值</span><span class="sxs-lookup"><span data-stu-id="6062b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6062b-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6062b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6062b-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6062b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6062b-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6062b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6062b-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="6062b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6062b-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="6062b-140">Namespace</span></span><br/>                | <span data-ttu-id="6062b-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6062b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6062b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6062b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6062b-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6062b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6062b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6062b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6062b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6062b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

