---
description: CIM \_ ActsAsSpare 關聯會指出哪些專案可以是可替換的元素，或是取代其他匯總的元素。 備用可以在 &0034 中操作 \# ; 熱待命&\# 0034; 模式，如同以元素為基礎所指定。
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936393"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="4dbe2-104">CIM \_ ActsAsSpare 類別</span><span class="sxs-lookup"><span data-stu-id="4dbe2-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="4dbe2-105">**CIM \_ ActsAsSpare** 關聯會指出哪些專案可以是可替換的元素，或是取代其他匯總的元素。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="4dbe2-106">備用可以依元素個別的指定，以「熱待命」模式運作。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dbe2-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4dbe2-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4dbe2-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4dbe2-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbe2-111">語法</span><span class="sxs-lookup"><span data-stu-id="4dbe2-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="4dbe2-112">成員</span><span class="sxs-lookup"><span data-stu-id="4dbe2-112">Members</span></span>

<span data-ttu-id="4dbe2-113">**CIM \_ ActsAsSpare** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4dbe2-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="4dbe2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4dbe2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dbe2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4dbe2-115">Properties</span></span>

<span data-ttu-id="4dbe2-116">**CIM \_ ActsAsSpare** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dbe2-117">**群組**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbe2-118">資料類型： **CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="4dbe2-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dbe2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dbe2-120">代表 [**CIM \_ SpareGroup**](cim-sparegroup.md)類別之 **群組** 屬性的參考。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4dbe2-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbe2-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4dbe2-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dbe2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dbe2-124">若為 **TRUE**，則會以熱待命的形式操作備用。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="4dbe2-125">**備用**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbe2-126">資料類型： **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="4dbe2-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4dbe2-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4dbe2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dbe2-128">參考受管理的系統專案，此專案會作為備用並參與備用群組。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dbe2-129">備註</span><span class="sxs-lookup"><span data-stu-id="4dbe2-129">Remarks</span></span>

<span data-ttu-id="4dbe2-130">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-130">WMI does not implement this class.</span></span>

<span data-ttu-id="4dbe2-131">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4dbe2-132">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4dbe2-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dbe2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dbe2-133">Requirements</span></span>



| <span data-ttu-id="4dbe2-134">需求</span><span class="sxs-lookup"><span data-stu-id="4dbe2-134">Requirement</span></span> | <span data-ttu-id="4dbe2-135">值</span><span class="sxs-lookup"><span data-stu-id="4dbe2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dbe2-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dbe2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4dbe2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4dbe2-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4dbe2-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dbe2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4dbe2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dbe2-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4dbe2-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="4dbe2-140">Namespace</span></span><br/>                | <span data-ttu-id="4dbe2-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4dbe2-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4dbe2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4dbe2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dbe2-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dbe2-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dbe2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4dbe2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dbe2-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dbe2-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dbe2-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dbe2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dbe2-147">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="4dbe2-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

