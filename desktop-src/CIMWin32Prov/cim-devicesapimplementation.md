---
description: CIM \_ DeviceSAPImplementation 類別代表服務存取點 (SAP) 與其實作為方式之間的關聯。
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: 'CIM_DeviceSAPImplementation 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689027"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="cb12b-103">CIM_DeviceSAPImplementation 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="cb12b-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cb12b-104">**CIM \_ DeviceSAPImplementation** 類別代表服務存取點 (SAP) 與其實作為方式之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="cb12b-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="cb12b-105">當許多邏輯裝置與一個 SAP 相關聯時，這些專案會一起運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="cb12b-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="cb12b-106">如果有不同的 SAP 執行，每個實施都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="cb12b-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb12b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cb12b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb12b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cb12b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb12b-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb12b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cb12b-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cb12b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb12b-111">語法</span><span class="sxs-lookup"><span data-stu-id="cb12b-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="cb12b-112">成員</span><span class="sxs-lookup"><span data-stu-id="cb12b-112">Members</span></span>

<span data-ttu-id="cb12b-113">**CIM \_ DeviceSAPImplementation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cb12b-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="cb12b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="cb12b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb12b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="cb12b-115">Properties</span></span>

<span data-ttu-id="cb12b-116">**CIM \_ DeviceSAPImplementation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cb12b-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb12b-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="cb12b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb12b-118">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="cb12b-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="cb12b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb12b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb12b-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="cb12b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cb12b-121">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb12b-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cb12b-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="cb12b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb12b-123">資料類型： **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="cb12b-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="cb12b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cb12b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb12b-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="cb12b-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cb12b-126">[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ，描述使用邏輯裝置所執行的服務存取點。</span><span class="sxs-lookup"><span data-stu-id="cb12b-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb12b-127">備註</span><span class="sxs-lookup"><span data-stu-id="cb12b-127">Remarks</span></span>

<span data-ttu-id="cb12b-128">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cb12b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="cb12b-129">**Cim \_ DeviceSAPImplementation** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="cb12b-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cb12b-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cb12b-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb12b-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cb12b-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb12b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb12b-132">Requirements</span></span>



| <span data-ttu-id="cb12b-133">需求</span><span class="sxs-lookup"><span data-stu-id="cb12b-133">Requirement</span></span> | <span data-ttu-id="cb12b-134">值</span><span class="sxs-lookup"><span data-stu-id="cb12b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb12b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb12b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cb12b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb12b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb12b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb12b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cb12b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb12b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb12b-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb12b-139">Namespace</span></span><br/>                | <span data-ttu-id="cb12b-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cb12b-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb12b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cb12b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb12b-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb12b-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb12b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cb12b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb12b-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb12b-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb12b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb12b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb12b-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="cb12b-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

