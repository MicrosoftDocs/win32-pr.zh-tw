---
description: CIM \_ ComputerSystemDMA 類別代表電腦系統與其可用的直接記憶體存取 (DMA) 通道之間的關聯。
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: CIM_ComputerSystemDMA 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973782"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="7bf26-103">CIM \_ ComputerSystemDMA 類別</span><span class="sxs-lookup"><span data-stu-id="7bf26-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="7bf26-104">**CIM \_ ComputerSystemDMA** 類別代表電腦系統與其可用的直接記憶體存取 (DMA) 通道之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="7bf26-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf26-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7bf26-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7bf26-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7bf26-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7bf26-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7bf26-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7bf26-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7bf26-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf26-109">語法</span><span class="sxs-lookup"><span data-stu-id="7bf26-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7bf26-110">成員</span><span class="sxs-lookup"><span data-stu-id="7bf26-110">Members</span></span>

<span data-ttu-id="7bf26-111">**CIM \_ ComputerSystemDMA** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7bf26-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="7bf26-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7bf26-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bf26-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7bf26-113">Properties</span></span>

<span data-ttu-id="7bf26-114">**CIM \_ ComputerSystemDMA** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7bf26-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bf26-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7bf26-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bf26-116">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="7bf26-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7bf26-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bf26-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bf26-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="7bf26-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7bf26-119">一個 [**CIM \_**](cim-computersystem.md) 的電腦，描述與 DMA 相關聯的電腦。</span><span class="sxs-lookup"><span data-stu-id="7bf26-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="7bf26-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7bf26-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bf26-121">資料類型： **CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="7bf26-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="7bf26-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bf26-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bf26-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="7bf26-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bf26-124">描述電腦系統 DMA 通道的 [**CIM \_ DMA**](cim-dma.md) 。</span><span class="sxs-lookup"><span data-stu-id="7bf26-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bf26-125">備註</span><span class="sxs-lookup"><span data-stu-id="7bf26-125">Remarks</span></span>

<span data-ttu-id="7bf26-126">**Cim \_ ComputerSystemDMA** 類別衍生自 [**cim \_ ComputerSystemResource**](cim-computersystemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="7bf26-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="7bf26-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7bf26-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7bf26-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7bf26-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7bf26-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7bf26-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf26-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bf26-130">Requirements</span></span>



| <span data-ttu-id="7bf26-131">需求</span><span class="sxs-lookup"><span data-stu-id="7bf26-131">Requirement</span></span> | <span data-ttu-id="7bf26-132">值</span><span class="sxs-lookup"><span data-stu-id="7bf26-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf26-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bf26-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf26-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bf26-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bf26-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bf26-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf26-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bf26-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bf26-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="7bf26-137">Namespace</span></span><br/>                | <span data-ttu-id="7bf26-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7bf26-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bf26-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7bf26-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bf26-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bf26-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bf26-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7bf26-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bf26-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bf26-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf26-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bf26-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf26-144">**CIM \_ ComputerSystemResource**</span><span class="sxs-lookup"><span data-stu-id="7bf26-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

