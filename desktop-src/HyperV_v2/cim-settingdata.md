---
description: 代表 CIM ManagedElement 實例的設定和指令引數 \_ 。
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193324"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="e990f-103">CIM \_ SettingData 類別</span><span class="sxs-lookup"><span data-stu-id="e990f-103">CIM\_SettingData class</span></span>

<span data-ttu-id="e990f-104">代表 [**CIM \_ ManagedElement**](cim-managedelement.md) 實例的設定和指令引數。</span><span class="sxs-lookup"><span data-stu-id="e990f-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="e990f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e990f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="e990f-106">成員</span><span class="sxs-lookup"><span data-stu-id="e990f-106">Members</span></span>

<span data-ttu-id="e990f-107">**CIM \_ SettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e990f-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e990f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e990f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e990f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e990f-109">Properties</span></span>

<span data-ttu-id="e990f-110">**CIM \_ SettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e990f-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e990f-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e990f-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e990f-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e990f-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e990f-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e990f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e990f-114">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="e990f-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="e990f-115">這個類別之實例的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="e990f-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="e990f-116">此外，使用者易記名稱可用來做為搜尋或查詢的索引。</span><span class="sxs-lookup"><span data-stu-id="e990f-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="e990f-117">名稱在命名空間中不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e990f-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="e990f-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e990f-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e990f-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e990f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e990f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e990f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e990f-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="e990f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="e990f-122">在包含的命名空間範圍內唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e990f-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e990f-123">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="e990f-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="e990f-124">*OrgID* 必須包含受著作權、商標或其他唯一的名稱，該名稱是由定義 **InstanceID** 屬性的商業實體所擁有，或是由可辨識的全域授權單位指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="e990f-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="e990f-125">*OrgID* 不能包含冒號。</span><span class="sxs-lookup"><span data-stu-id="e990f-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="e990f-126">**InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="e990f-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="e990f-127">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="e990f-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="e990f-128">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="e990f-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="e990f-129">針對已定義的 DMTF 實例，必須搭配 *OrgID* 設定為 "CIM" 的模式使用。</span><span class="sxs-lookup"><span data-stu-id="e990f-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e990f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e990f-130">Requirements</span></span>



| <span data-ttu-id="e990f-131">需求</span><span class="sxs-lookup"><span data-stu-id="e990f-131">Requirement</span></span> | <span data-ttu-id="e990f-132">值</span><span class="sxs-lookup"><span data-stu-id="e990f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e990f-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e990f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e990f-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e990f-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e990f-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e990f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e990f-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e990f-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e990f-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="e990f-137">Namespace</span></span><br/>                | <span data-ttu-id="e990f-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e990f-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e990f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e990f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e990f-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e990f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e990f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e990f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e990f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e990f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e990f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e990f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e990f-144">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e990f-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

