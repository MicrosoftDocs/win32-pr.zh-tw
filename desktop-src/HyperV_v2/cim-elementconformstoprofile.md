---
description: 代表 managed 專案符合已註冊設定檔之標準的關聯。
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: CIM_ElementConformsToProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967176"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="dad10-103">CIM \_ ElementConformsToProfile 類別</span><span class="sxs-lookup"><span data-stu-id="dad10-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="dad10-104">代表 managed 專案符合已註冊設定檔之標準的關聯。</span><span class="sxs-lookup"><span data-stu-id="dad10-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="dad10-105">此關聯通常會套用至較高層級的實例，例如系統、命名空間或服務。</span><span class="sxs-lookup"><span data-stu-id="dad10-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="dad10-106">當套用至較高層級的實例時，所有組成零件都必須適當地運作，以支援 ManagedElement 與命名 RegisteredProfile 的一致性。</span><span class="sxs-lookup"><span data-stu-id="dad10-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad10-107">語法</span><span class="sxs-lookup"><span data-stu-id="dad10-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="dad10-108">成員</span><span class="sxs-lookup"><span data-stu-id="dad10-108">Members</span></span>

<span data-ttu-id="dad10-109">**CIM \_ ElementConformsToProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dad10-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="dad10-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dad10-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dad10-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dad10-111">Properties</span></span>

<span data-ttu-id="dad10-112">**CIM \_ ElementConformsToProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dad10-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dad10-113">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="dad10-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad10-114">資料類型： **CIM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="dad10-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="dad10-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dad10-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad10-116">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dad10-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dad10-117">受管理元素符合的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="dad10-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="dad10-118">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="dad10-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dad10-119">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="dad10-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="dad10-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dad10-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dad10-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dad10-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dad10-122">符合已註冊設定檔的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="dad10-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dad10-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dad10-123">Requirements</span></span>



| <span data-ttu-id="dad10-124">需求</span><span class="sxs-lookup"><span data-stu-id="dad10-124">Requirement</span></span> | <span data-ttu-id="dad10-125">值</span><span class="sxs-lookup"><span data-stu-id="dad10-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad10-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dad10-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dad10-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dad10-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dad10-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dad10-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dad10-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dad10-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dad10-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="dad10-130">Namespace</span></span><br/>                | <span data-ttu-id="dad10-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="dad10-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dad10-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dad10-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dad10-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dad10-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dad10-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dad10-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad10-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dad10-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

