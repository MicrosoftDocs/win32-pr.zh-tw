---
description: 子類別的抽象類別，描述相關聯之受管理元素的能力，以及可能的能力。
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997542"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="6953c-103">CIM \_ 功能類別</span><span class="sxs-lookup"><span data-stu-id="6953c-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="6953c-104">子類別的抽象類別，描述相關聯之受管理元素的能力，以及可能的能力。</span><span class="sxs-lookup"><span data-stu-id="6953c-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="6953c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6953c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="6953c-106">成員</span><span class="sxs-lookup"><span data-stu-id="6953c-106">Members</span></span>

<span data-ttu-id="6953c-107">**CIM \_ 功能** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6953c-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6953c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="6953c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6953c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6953c-109">Properties</span></span>

<span data-ttu-id="6953c-110">**CIM \_ 功能** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6953c-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6953c-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6953c-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6953c-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6953c-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6953c-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6953c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6953c-114">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="6953c-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="6953c-115">這個類別實例的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="6953c-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="6953c-116">此外，使用者易記名稱也可以當做查詢的索引屬性使用。</span><span class="sxs-lookup"><span data-stu-id="6953c-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="6953c-117">此值在其命名空間中不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6953c-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="6953c-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6953c-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6953c-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6953c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6953c-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6953c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6953c-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="6953c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="6953c-122">在包含的命名空間範圍內，以獨特且不透明的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6953c-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6953c-123">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="6953c-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="6953c-124">*OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="6953c-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="6953c-125">此模式類似于架構類別名稱的結構。</span><span class="sxs-lookup"><span data-stu-id="6953c-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="6953c-126">此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="6953c-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="6953c-127">因此， *OrgID* 不能包含冒號 ( '： ' ) 。</span><span class="sxs-lookup"><span data-stu-id="6953c-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="6953c-128">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="6953c-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="6953c-129">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="6953c-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="6953c-130">若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。</span><span class="sxs-lookup"><span data-stu-id="6953c-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6953c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6953c-131">Requirements</span></span>



| <span data-ttu-id="6953c-132">需求</span><span class="sxs-lookup"><span data-stu-id="6953c-132">Requirement</span></span> | <span data-ttu-id="6953c-133">值</span><span class="sxs-lookup"><span data-stu-id="6953c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6953c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6953c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6953c-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6953c-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6953c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6953c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6953c-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6953c-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6953c-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="6953c-138">Namespace</span></span><br/>                | <span data-ttu-id="6953c-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6953c-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6953c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6953c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6953c-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6953c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6953c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6953c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6953c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6953c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6953c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6953c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6953c-145">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6953c-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

