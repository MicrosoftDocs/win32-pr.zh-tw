---
description: 定義參考的獨立系統所符合的已註冊設定檔。
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943772"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="3ecbb-103">Msvm \_ StandaloneV2ElementConformsToProfile 類別</span><span class="sxs-lookup"><span data-stu-id="3ecbb-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="3ecbb-104">定義參考的獨立系統所符合的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ecbb-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="3ecbb-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3ecbb-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecbb-106">語法</span><span class="sxs-lookup"><span data-stu-id="3ecbb-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="3ecbb-107">成員</span><span class="sxs-lookup"><span data-stu-id="3ecbb-107">Members</span></span>

<span data-ttu-id="3ecbb-108">**Msvm \_ StandaloneV2ElementConformsToProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ecbb-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="3ecbb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3ecbb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ecbb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3ecbb-110">Properties</span></span>

<span data-ttu-id="3ecbb-111">**Msvm \_ StandaloneV2ElementConformsToProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3ecbb-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ecbb-112">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="3ecbb-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ecbb-113">資料類型： **Msvm \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="3ecbb-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="3ecbb-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ecbb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ecbb-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3ecbb-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3ecbb-116">獨立系統符合的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ecbb-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="3ecbb-117">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="3ecbb-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ecbb-118">資料類型： **Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="3ecbb-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3ecbb-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ecbb-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ecbb-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)、 **MSFT \_ TargetNamespace** ( 「根 \\ \\ 虛擬化 \\ \\ v2」 ) </span><span class="sxs-lookup"><span data-stu-id="3ecbb-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="3ecbb-121">符合已註冊設定檔的獨立系統。</span><span class="sxs-lookup"><span data-stu-id="3ecbb-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ecbb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ecbb-122">Requirements</span></span>



| <span data-ttu-id="3ecbb-123">需求</span><span class="sxs-lookup"><span data-stu-id="3ecbb-123">Requirement</span></span> | <span data-ttu-id="3ecbb-124">值</span><span class="sxs-lookup"><span data-stu-id="3ecbb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecbb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ecbb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecbb-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ecbb-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3ecbb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ecbb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecbb-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3ecbb-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3ecbb-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ecbb-129">Namespace</span></span><br/>                | <span data-ttu-id="3ecbb-130">根 \\ interop</span><span class="sxs-lookup"><span data-stu-id="3ecbb-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="3ecbb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3ecbb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ecbb-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3ecbb-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ecbb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3ecbb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ecbb-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ecbb-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ecbb-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ecbb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecbb-136">**Msvm \_ ElementConformsToProfile**</span><span class="sxs-lookup"><span data-stu-id="3ecbb-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

