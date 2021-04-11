---
description: CIM \_ CollectedCollections 類別是一種匯總關聯，代表 mse 集合中所包含之受管理系統元素 (MSE) 。
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936361"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="823ad-103">CIM \_ CollectedCollections 類別</span><span class="sxs-lookup"><span data-stu-id="823ad-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="823ad-104">**CIM \_ CollectedCollections** 類別是一種匯總關聯，代表 mse 集合中所包含之受管理系統元素 (MSE) 。</span><span class="sxs-lookup"><span data-stu-id="823ad-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="823ad-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="823ad-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="823ad-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="823ad-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="823ad-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="823ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="823ad-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="823ad-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="823ad-109">語法</span><span class="sxs-lookup"><span data-stu-id="823ad-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="823ad-110">成員</span><span class="sxs-lookup"><span data-stu-id="823ad-110">Members</span></span>

<span data-ttu-id="823ad-111">**CIM \_ CollectedCollections** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="823ad-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="823ad-112">屬性</span><span class="sxs-lookup"><span data-stu-id="823ad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="823ad-113">屬性</span><span class="sxs-lookup"><span data-stu-id="823ad-113">Properties</span></span>

<span data-ttu-id="823ad-114">**CIM \_ CollectedCollections** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="823ad-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="823ad-115">**集合**</span><span class="sxs-lookup"><span data-stu-id="823ad-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ad-116">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="823ad-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="823ad-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823ad-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ad-118">對匯總中「較高層級」或父元素的參考。</span><span class="sxs-lookup"><span data-stu-id="823ad-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="823ad-119">**CollectionInCollection**</span><span class="sxs-lookup"><span data-stu-id="823ad-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ad-120">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="823ad-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="823ad-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823ad-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ad-122">「收集」 **集合** 的參考。</span><span class="sxs-lookup"><span data-stu-id="823ad-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="823ad-123">備註</span><span class="sxs-lookup"><span data-stu-id="823ad-123">Remarks</span></span>

<span data-ttu-id="823ad-124">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="823ad-124">WMI does not implement this class.</span></span>

<span data-ttu-id="823ad-125">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="823ad-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="823ad-126">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="823ad-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="823ad-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="823ad-127">Requirements</span></span>



| <span data-ttu-id="823ad-128">需求</span><span class="sxs-lookup"><span data-stu-id="823ad-128">Requirement</span></span> | <span data-ttu-id="823ad-129">值</span><span class="sxs-lookup"><span data-stu-id="823ad-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="823ad-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="823ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="823ad-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823ad-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="823ad-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="823ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="823ad-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="823ad-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="823ad-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="823ad-134">Namespace</span></span><br/>                | <span data-ttu-id="823ad-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="823ad-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="823ad-136">MOF</span><span class="sxs-lookup"><span data-stu-id="823ad-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823ad-137"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="823ad-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="823ad-138">DLL</span><span class="sxs-lookup"><span data-stu-id="823ad-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823ad-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823ad-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




