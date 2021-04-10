---
description: CIM \_ CollectionOfMSEs 物件允許將 cim \_ ManagedSystemElement 物件分組，以建立設定和設定的關聯性。 它是抽象的，需要在子類別中進行進一步的定義和語義改進。
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: 'CIM_CollectionOfMSEs 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110993"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="3f31a-104">CIM_CollectionOfMSEs 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="3f31a-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3f31a-105">**Cim \_ CollectionOfMSEs** 物件允許將 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件分組，以建立設定和設定的關聯性。</span><span class="sxs-lookup"><span data-stu-id="3f31a-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="3f31a-106">它是抽象的，需要在子類別中進行進一步的定義和語義改進。</span><span class="sxs-lookup"><span data-stu-id="3f31a-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="3f31a-107">**CIM \_ CollectionOfMSEs** 物件不會包含任何狀態或狀態資訊，但只代表元素群組。</span><span class="sxs-lookup"><span data-stu-id="3f31a-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="3f31a-108">基於這個理由，從 **cim \_ CollectionOfMSEs** 具有狀態/狀態的子類別化群組不正確，例如 [**Cim \_ RedundancyGroup**](cim-redundancygroup.md) (從 [**cim \_ LogicalElement**](cim-logicalelement.md)) 正確子類別。</span><span class="sxs-lookup"><span data-stu-id="3f31a-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="3f31a-109">集合通常會匯總「贊」物件，並表示優化。</span><span class="sxs-lookup"><span data-stu-id="3f31a-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="3f31a-110">如果沒有集合，則會強制定義個別的 [**cim \_ ElementSetting**](cim-elementsetting.md) 和 [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) 關聯，以將設定和設定物件系結至個別的 [**cim \_ ManagedSystemElements**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3f31a-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="3f31a-111">將相同的設定指派給多個物件時，可能會有很多重複。</span><span class="sxs-lookup"><span data-stu-id="3f31a-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="3f31a-112">此外，使用 collection 物件可判斷集合成員的設定和設定關聯確實相同。</span><span class="sxs-lookup"><span data-stu-id="3f31a-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="3f31a-113">這項資訊的取得方式是以專屬的方式定義集合，然後查詢 **CIM \_ ElementSetting** 和 **cim \_ ElementConfiguration** 關聯，以判斷是否已完全涵蓋該收集組。</span><span class="sxs-lookup"><span data-stu-id="3f31a-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f31a-114">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3f31a-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3f31a-115">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3f31a-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3f31a-116">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f31a-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3f31a-117">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3f31a-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f31a-118">語法</span><span class="sxs-lookup"><span data-stu-id="3f31a-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="3f31a-119">成員</span><span class="sxs-lookup"><span data-stu-id="3f31a-119">Members</span></span>

<span data-ttu-id="3f31a-120">**CIM \_ CollectionOfMSEs** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f31a-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="3f31a-121">屬性</span><span class="sxs-lookup"><span data-stu-id="3f31a-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f31a-122">屬性</span><span class="sxs-lookup"><span data-stu-id="3f31a-122">Properties</span></span>

<span data-ttu-id="3f31a-123">**CIM \_ CollectionOfMSEs** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3f31a-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f31a-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="3f31a-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f31a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f31a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-127">CollectionOfMSEs 物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3f31a-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-128">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="3f31a-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f31a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f31a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-131">集合物件的識別。</span><span class="sxs-lookup"><span data-stu-id="3f31a-131">Identification of the Collection object.</span></span> <span data-ttu-id="3f31a-132">子類別化時，CollectionID 屬性可以覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="3f31a-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="3f31a-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="3f31a-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f31a-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f31a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f31a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f31a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f31a-136">CollectionOfMSEs 物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3f31a-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f31a-137">備註</span><span class="sxs-lookup"><span data-stu-id="3f31a-137">Remarks</span></span>

<span data-ttu-id="3f31a-138">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3f31a-138">WMI does not implement this class.</span></span> <span data-ttu-id="3f31a-139">請參閱衍生自 **CIM \_ COLLECTIONOFMSES** 之 WMI 類別的 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3f31a-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="3f31a-140">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3f31a-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3f31a-141">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3f31a-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f31a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f31a-142">Requirements</span></span>



| <span data-ttu-id="3f31a-143">需求</span><span class="sxs-lookup"><span data-stu-id="3f31a-143">Requirement</span></span> | <span data-ttu-id="3f31a-144">值</span><span class="sxs-lookup"><span data-stu-id="3f31a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f31a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f31a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3f31a-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f31a-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f31a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f31a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3f31a-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f31a-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f31a-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="3f31a-149">Namespace</span></span><br/>                | <span data-ttu-id="3f31a-150">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3f31a-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3f31a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="3f31a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f31a-152"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f31a-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f31a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3f31a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f31a-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f31a-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




