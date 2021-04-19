---
description: 將 Msvm \_ ReferencePointCollection 與對應的 Msvm \_ VirtualSystemCollection 物件產生關聯。
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Msvm_ReferencePointOfVirtualSystemCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981597"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="8e854-103">Msvm \_ ReferencePointOfVirtualSystemCollection 類別</span><span class="sxs-lookup"><span data-stu-id="8e854-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="8e854-104">將 [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) 與對應的 [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8e854-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="8e854-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e854-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e854-106">語法</span><span class="sxs-lookup"><span data-stu-id="8e854-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8e854-107">成員</span><span class="sxs-lookup"><span data-stu-id="8e854-107">Members</span></span>

<span data-ttu-id="8e854-108">**Msvm \_ ReferencePointOfVirtualSystemCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e854-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="8e854-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8e854-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e854-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8e854-110">Properties</span></span>

<span data-ttu-id="8e854-111">**Msvm \_ ReferencePointOfVirtualSystemCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e854-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e854-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="8e854-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e854-113">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="8e854-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="8e854-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e854-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e854-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="8e854-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8e854-116">[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) ，表示此關聯中的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="8e854-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="8e854-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8e854-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e854-118">資料類型： **CIM \_ 集合**</span><span class="sxs-lookup"><span data-stu-id="8e854-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="8e854-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e854-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e854-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="8e854-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8e854-121">[**CIM \_ 集合**](cim-collection.md)，表示相依于 **前面** 的物件。</span><span class="sxs-lookup"><span data-stu-id="8e854-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e854-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e854-122">Requirements</span></span>



| <span data-ttu-id="8e854-123">需求</span><span class="sxs-lookup"><span data-stu-id="8e854-123">Requirement</span></span> | <span data-ttu-id="8e854-124">值</span><span class="sxs-lookup"><span data-stu-id="8e854-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e854-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e854-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8e854-126">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e854-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8e854-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e854-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8e854-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8e854-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8e854-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e854-129">Namespace</span></span><br/>                | <span data-ttu-id="8e854-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e854-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e854-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8e854-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e854-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8e854-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e854-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8e854-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e854-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e854-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e854-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e854-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e854-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="8e854-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

