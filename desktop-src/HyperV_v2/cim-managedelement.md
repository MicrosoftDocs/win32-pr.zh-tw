---
description: CIM \_ ManagedElement 類別是一種抽象類別，可針對 CIM 架構中的非關聯類別，提供通用超類別 (或繼承樹狀結構的最上層) 。
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973602"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="2f584-103">CIM \_ ManagedElement 類別</span><span class="sxs-lookup"><span data-stu-id="2f584-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="2f584-104">**Cim \_ ManagedElement** 類別是一種抽象類別，可針對 CIM 架構中的非關聯類別，提供通用超類別 (或繼承樹狀結構的最上層) 。</span><span class="sxs-lookup"><span data-stu-id="2f584-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f584-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f584-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="2f584-106">成員</span><span class="sxs-lookup"><span data-stu-id="2f584-106">Members</span></span>

<span data-ttu-id="2f584-107">**CIM \_ ManagedElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f584-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="2f584-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2f584-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f584-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2f584-109">Properties</span></span>

<span data-ttu-id="2f584-110">**CIM \_ ManagedElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f584-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f584-111">**標題**</span><span class="sxs-lookup"><span data-stu-id="2f584-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f584-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f584-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f584-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f584-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f584-114">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2f584-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2f584-115">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f584-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2f584-116">**說明**</span><span class="sxs-lookup"><span data-stu-id="2f584-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f584-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f584-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f584-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f584-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f584-119">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f584-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="2f584-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2f584-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f584-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f584-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f584-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f584-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f584-123">物件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="2f584-123">A user-friendly name for the object.</span></span> <span data-ttu-id="2f584-124">這個屬性可讓每個實例定義使用者易記名稱，以及其索引鍵屬性、身分識別資料和描述資訊。</span><span class="sxs-lookup"><span data-stu-id="2f584-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="2f584-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f584-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f584-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f584-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f584-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f584-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f584-128">在包含的命名空間範圍內，以獨特且不透明的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2f584-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2f584-129">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="2f584-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="2f584-130">*OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f584-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="2f584-131">此模式類似于架構類別名稱的結構。</span><span class="sxs-lookup"><span data-stu-id="2f584-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="2f584-132">此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="2f584-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="2f584-133">因此， *OrgID* 不能包含冒號 ( '： ' ) 。</span><span class="sxs-lookup"><span data-stu-id="2f584-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="2f584-134">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="2f584-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="2f584-135">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="2f584-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="2f584-136">若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。</span><span class="sxs-lookup"><span data-stu-id="2f584-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f584-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f584-137">Requirements</span></span>



| <span data-ttu-id="2f584-138">需求</span><span class="sxs-lookup"><span data-stu-id="2f584-138">Requirement</span></span> | <span data-ttu-id="2f584-139">值</span><span class="sxs-lookup"><span data-stu-id="2f584-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f584-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f584-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2f584-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f584-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2f584-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f584-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2f584-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f584-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2f584-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f584-144">Namespace</span></span><br/>                | <span data-ttu-id="2f584-145">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f584-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f584-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2f584-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f584-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2f584-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f584-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2f584-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f584-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f584-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

