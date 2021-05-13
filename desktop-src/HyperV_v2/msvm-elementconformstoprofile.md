---
description: 定義所參考系統符合的已註冊設定檔。
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843279"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="00763-103">Msvm \_ ElementConformsToProfile 類別</span><span class="sxs-lookup"><span data-stu-id="00763-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="00763-104">定義所參考系統符合的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="00763-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="00763-105">這個關聯可能會套用至任何 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="00763-105">This association may apply to any managed element.</span></span> <span data-ttu-id="00763-106">一般使用方式會將它套用至較高層級的實例，例如系統、命名空間或服務。</span><span class="sxs-lookup"><span data-stu-id="00763-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="00763-107">當套用至較高層級的實例時，所有組成零件都必須適當地運作，以支援受管理元素與已命名之註冊設定檔的一致性。</span><span class="sxs-lookup"><span data-stu-id="00763-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="00763-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="00763-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00763-109">語法</span><span class="sxs-lookup"><span data-stu-id="00763-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="00763-110">成員</span><span class="sxs-lookup"><span data-stu-id="00763-110">Members</span></span>

<span data-ttu-id="00763-111">**Msvm \_ ElementConformsToProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="00763-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="00763-112">屬性</span><span class="sxs-lookup"><span data-stu-id="00763-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00763-113">屬性</span><span class="sxs-lookup"><span data-stu-id="00763-113">Properties</span></span>

<span data-ttu-id="00763-114">**Msvm \_ ElementConformsToProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="00763-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00763-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="00763-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00763-116">資料類型： **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="00763-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="00763-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="00763-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00763-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00763-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00763-119">[**Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)類別實例的參考，表示系統符合的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="00763-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="00763-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="00763-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00763-121">資料類型： **[ **Msvm \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="00763-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="00763-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="00763-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00763-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00763-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00763-124">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表符合已註冊設定檔的系統。</span><span class="sxs-lookup"><span data-stu-id="00763-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00763-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="00763-125">Requirements</span></span>



| <span data-ttu-id="00763-126">需求</span><span class="sxs-lookup"><span data-stu-id="00763-126">Requirement</span></span> | <span data-ttu-id="00763-127">值</span><span class="sxs-lookup"><span data-stu-id="00763-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00763-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00763-128">Minimum supported client</span></span><br/> | <span data-ttu-id="00763-129">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00763-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="00763-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00763-130">Minimum supported server</span></span><br/> | <span data-ttu-id="00763-131">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00763-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00763-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="00763-132">Namespace</span></span><br/>                | <span data-ttu-id="00763-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="00763-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="00763-134">MOF</span><span class="sxs-lookup"><span data-stu-id="00763-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00763-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="00763-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00763-136">DLL</span><span class="sxs-lookup"><span data-stu-id="00763-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00763-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00763-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

