---
description: CIM \_ LinkHasConnector 類別會將用來作為實體連接器的纜線和連結（連接實體元素）相關聯。 此關聯會明確定義適用于 CIM PhysicalLink 之連接器的關聯性 \_ 。
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: CIM_LinkHasConnector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847351"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="ce57f-104">CIM \_ LinkHasConnector 類別</span><span class="sxs-lookup"><span data-stu-id="ce57f-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="ce57f-105">**CIM \_ LinkHasConnector** 類別會將用來作為實體連接器的纜線和連結（連接實體元素）相關聯。</span><span class="sxs-lookup"><span data-stu-id="ce57f-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="ce57f-106">此關聯會明確定義適用于 [**CIM \_ PhysicalLink**](cim-physicallink.md)之連接器的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ce57f-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce57f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="ce57f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce57f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="ce57f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce57f-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ce57f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ce57f-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ce57f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce57f-111">語法</span><span class="sxs-lookup"><span data-stu-id="ce57f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ce57f-112">成員</span><span class="sxs-lookup"><span data-stu-id="ce57f-112">Members</span></span>

<span data-ttu-id="ce57f-113">**CIM \_ LinkHasConnector** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ce57f-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="ce57f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ce57f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce57f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ce57f-115">Properties</span></span>

<span data-ttu-id="ce57f-116">**CIM \_ LinkHasConnector** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ce57f-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce57f-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ce57f-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce57f-118">資料類型： **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="ce57f-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="ce57f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce57f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce57f-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="ce57f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ce57f-121">[**CIM \_ PhysicalLink**](cim-physicallink.md) ，描述具有連接器的實體連結。</span><span class="sxs-lookup"><span data-stu-id="ce57f-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="ce57f-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ce57f-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce57f-123">資料類型： **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="ce57f-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="ce57f-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce57f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce57f-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="ce57f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ce57f-126">描述實體連接器的 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce57f-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce57f-127">備註</span><span class="sxs-lookup"><span data-stu-id="ce57f-127">Remarks</span></span>

<span data-ttu-id="ce57f-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="ce57f-128">WMI does not implement this class.</span></span>

<span data-ttu-id="ce57f-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="ce57f-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce57f-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ce57f-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce57f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce57f-131">Requirements</span></span>



| <span data-ttu-id="ce57f-132">需求</span><span class="sxs-lookup"><span data-stu-id="ce57f-132">Requirement</span></span> | <span data-ttu-id="ce57f-133">值</span><span class="sxs-lookup"><span data-stu-id="ce57f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce57f-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce57f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce57f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce57f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce57f-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce57f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce57f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce57f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce57f-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce57f-138">Namespace</span></span><br/>                | <span data-ttu-id="ce57f-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ce57f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce57f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ce57f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce57f-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce57f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce57f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce57f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce57f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce57f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce57f-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce57f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce57f-145">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="ce57f-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

