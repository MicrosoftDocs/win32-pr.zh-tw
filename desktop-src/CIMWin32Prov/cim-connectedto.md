---
description: CIM \_ ConnectedTo 類別代表一種關聯，表示兩個或多個實體連接器已連線。
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: CIM_ConnectedTo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025950"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="2ecdd-103">CIM \_ ConnectedTo 類別</span><span class="sxs-lookup"><span data-stu-id="2ecdd-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="2ecdd-104">**CIM \_ ConnectedTo** 類別代表一種關聯，表示兩個或多個實體連接器已連線。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ecdd-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2ecdd-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2ecdd-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2ecdd-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecdd-109">語法</span><span class="sxs-lookup"><span data-stu-id="2ecdd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2ecdd-110">成員</span><span class="sxs-lookup"><span data-stu-id="2ecdd-110">Members</span></span>

<span data-ttu-id="2ecdd-111">**CIM \_ ConnectedTo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2ecdd-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="2ecdd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2ecdd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ecdd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2ecdd-113">Properties</span></span>

<span data-ttu-id="2ecdd-114">**CIM \_ ConnectedTo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ecdd-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="2ecdd-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ecdd-116">資料類型： **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="2ecdd-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="2ecdd-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2ecdd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ecdd-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="2ecdd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2ecdd-119">[**CIM \_ PhysicalConnector**](cim-physicalconnector.md) ，表示作為連線一端的實體連接器。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="2ecdd-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="2ecdd-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ecdd-121">資料類型： **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="2ecdd-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="2ecdd-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2ecdd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ecdd-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="2ecdd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2ecdd-124">表示另一個實體連接器的 [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) ，作為連線的另一端。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ecdd-125">備註</span><span class="sxs-lookup"><span data-stu-id="2ecdd-125">Remarks</span></span>

<span data-ttu-id="2ecdd-126">**Cim \_ ConnectedTo** 類別繼承自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2ecdd-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2ecdd-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2ecdd-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2ecdd-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecdd-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ecdd-130">Requirements</span></span>



| <span data-ttu-id="2ecdd-131">需求</span><span class="sxs-lookup"><span data-stu-id="2ecdd-131">Requirement</span></span> | <span data-ttu-id="2ecdd-132">值</span><span class="sxs-lookup"><span data-stu-id="2ecdd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecdd-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ecdd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecdd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ecdd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ecdd-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ecdd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecdd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ecdd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ecdd-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2ecdd-137">Namespace</span></span><br/>                | <span data-ttu-id="2ecdd-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2ecdd-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ecdd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2ecdd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ecdd-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ecdd-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ecdd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2ecdd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ecdd-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ecdd-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ecdd-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ecdd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ecdd-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="2ecdd-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

