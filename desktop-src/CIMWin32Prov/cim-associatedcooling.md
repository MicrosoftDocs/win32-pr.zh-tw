---
description: CIM \_ AssociatedCooling 關聯會指出風扇或其他冷卻裝置特定于裝置 (與提供主機殼或封包冷卻) 。
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111097"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="55e3a-103">CIM \_ AssociatedCooling 類別</span><span class="sxs-lookup"><span data-stu-id="55e3a-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="55e3a-104">**CIM \_ AssociatedCooling** 關聯會指出風扇或其他冷卻裝置特定于裝置 (與提供主機殼或封包冷卻) 。</span><span class="sxs-lookup"><span data-stu-id="55e3a-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="55e3a-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="55e3a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55e3a-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="55e3a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55e3a-107">語法</span><span class="sxs-lookup"><span data-stu-id="55e3a-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="55e3a-108">成員</span><span class="sxs-lookup"><span data-stu-id="55e3a-108">Members</span></span>

<span data-ttu-id="55e3a-109">**CIM \_ AssociatedCooling** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="55e3a-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="55e3a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="55e3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55e3a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="55e3a-111">Properties</span></span>

<span data-ttu-id="55e3a-112">**CIM \_ AssociatedCooling** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="55e3a-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55e3a-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="55e3a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e3a-114">資料類型： **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="55e3a-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="55e3a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55e3a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e3a-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="55e3a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="55e3a-117">描述冷卻裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="55e3a-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="55e3a-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="55e3a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55e3a-119">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="55e3a-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="55e3a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55e3a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55e3a-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="55e3a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="55e3a-122">參考要冷卻之邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="55e3a-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55e3a-123">備註</span><span class="sxs-lookup"><span data-stu-id="55e3a-123">Remarks</span></span>

<span data-ttu-id="55e3a-124">**Cim \_ AssociatedCooling** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="55e3a-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="55e3a-125">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="55e3a-125">WMI does not implement this class.</span></span>

<span data-ttu-id="55e3a-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="55e3a-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55e3a-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="55e3a-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e3a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="55e3a-128">Requirements</span></span>



| <span data-ttu-id="55e3a-129">需求</span><span class="sxs-lookup"><span data-stu-id="55e3a-129">Requirement</span></span> | <span data-ttu-id="55e3a-130">值</span><span class="sxs-lookup"><span data-stu-id="55e3a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55e3a-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55e3a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="55e3a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55e3a-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55e3a-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55e3a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="55e3a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55e3a-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55e3a-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="55e3a-135">Namespace</span></span><br/>                | <span data-ttu-id="55e3a-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55e3a-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55e3a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="55e3a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55e3a-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55e3a-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55e3a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="55e3a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55e3a-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55e3a-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e3a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55e3a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e3a-142">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="55e3a-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

