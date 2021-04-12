---
title: MDM_Policy_User_Result01_AttachmentManager02 類別
description: MDM \_ Policy \_ User \_ Result01 \_ AttachmentManager02 類別代表可用的附件管理員原則。
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- MDM_Policy_User_Result01_AttachmentManager02 類別
- MDM_Policy_User_Result01_AttachmentManager02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b78eadb9aa320d35d3a8078359a682536fd7e120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465425"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a><span data-ttu-id="e69c6-105">MDM \_ 原則 \_ 使用者 \_ Result01 \_ AttachmentManager02 類別</span><span class="sxs-lookup"><span data-stu-id="e69c6-105">MDM\_Policy\_User\_Result01\_AttachmentManager02 class</span></span>

<span data-ttu-id="e69c6-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e69c6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e69c6-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e69c6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e69c6-108">MDM \_ Policy \_ User \_ Result01 \_ AttachmentManager02 類別代表可用的附件管理員原則。</span><span class="sxs-lookup"><span data-stu-id="e69c6-108">The MDM\_Policy\_User\_Result01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="e69c6-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e69c6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69c6-110">語法</span><span class="sxs-lookup"><span data-stu-id="e69c6-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="e69c6-111">成員</span><span class="sxs-lookup"><span data-stu-id="e69c6-111">Members</span></span>

<span data-ttu-id="e69c6-112">**MDM \_ Policy \_ User \_ Result01 \_ AttachmentManager02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e69c6-112">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="e69c6-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e69c6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e69c6-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e69c6-114">Properties</span></span>

<span data-ttu-id="e69c6-115">**MDM \_ Policy \_ User \_ Result01 \_ AttachmentManager02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e69c6-115">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e69c6-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="e69c6-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69c6-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e69c6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e69c6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e69c6-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="e69c6-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69c6-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e69c6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e69c6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e69c6-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e69c6-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69c6-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e69c6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e69c6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e69c6-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e69c6-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="e69c6-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69c6-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e69c6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e69c6-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e69c6-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e69c6-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e69c6-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e69c6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e69c6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e69c6-132">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e69c6-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e69c6-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e69c6-133">Requirements</span></span>



| <span data-ttu-id="e69c6-134">需求</span><span class="sxs-lookup"><span data-stu-id="e69c6-134">Requirement</span></span> | <span data-ttu-id="e69c6-135">值</span><span class="sxs-lookup"><span data-stu-id="e69c6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69c6-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e69c6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e69c6-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e69c6-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e69c6-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e69c6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e69c6-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="e69c6-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e69c6-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="e69c6-140">Namespace</span></span><br/>                | <span data-ttu-id="e69c6-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e69c6-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e69c6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e69c6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e69c6-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e69c6-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e69c6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e69c6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e69c6-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e69c6-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

