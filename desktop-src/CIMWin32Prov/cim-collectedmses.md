---
description: CIM \_ CollectedMSEs 關聯類別代表群組物件的成員（CollectionOfMSEs 類別）。
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: 'CIM_CollectedMSEs 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468357"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="1998b-103">CIM_CollectedMSEs 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="1998b-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1998b-104">**CIM \_ CollectedMSEs** 關聯類別代表群組物件的成員（ [**CollectionOfMSEs**](cim-collectionofmses.md)類別）。</span><span class="sxs-lookup"><span data-stu-id="1998b-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1998b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1998b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1998b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1998b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1998b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1998b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1998b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1998b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1998b-109">語法</span><span class="sxs-lookup"><span data-stu-id="1998b-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="1998b-110">成員</span><span class="sxs-lookup"><span data-stu-id="1998b-110">Members</span></span>

<span data-ttu-id="1998b-111">**CIM \_ CollectedMSEs** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1998b-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="1998b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1998b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1998b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1998b-113">Properties</span></span>

<span data-ttu-id="1998b-114">**CIM \_ CollectedMSEs** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1998b-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1998b-115">**集合**</span><span class="sxs-lookup"><span data-stu-id="1998b-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1998b-116">資料類型： **CM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="1998b-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="1998b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1998b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1998b-118">代表集合之群組或 "包" 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1998b-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="1998b-119">**成員**</span><span class="sxs-lookup"><span data-stu-id="1998b-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1998b-120">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1998b-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1998b-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1998b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1998b-122">集合成員的參考。</span><span class="sxs-lookup"><span data-stu-id="1998b-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1998b-123">備註</span><span class="sxs-lookup"><span data-stu-id="1998b-123">Remarks</span></span>

<span data-ttu-id="1998b-124">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1998b-124">WMI does not implement this class.</span></span> <span data-ttu-id="1998b-125">如需衍生自 **CIM \_ COLLECTEDMSES** 之 WMI 類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1998b-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1998b-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1998b-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1998b-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1998b-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1998b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1998b-128">Requirements</span></span>



| <span data-ttu-id="1998b-129">需求</span><span class="sxs-lookup"><span data-stu-id="1998b-129">Requirement</span></span> | <span data-ttu-id="1998b-130">值</span><span class="sxs-lookup"><span data-stu-id="1998b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1998b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1998b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1998b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1998b-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1998b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1998b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1998b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1998b-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1998b-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="1998b-135">Namespace</span></span><br/>                | <span data-ttu-id="1998b-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1998b-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1998b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1998b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1998b-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1998b-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1998b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1998b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1998b-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1998b-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




