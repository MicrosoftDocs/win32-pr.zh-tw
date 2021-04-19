---
description: CIM \_ SystemDevice 關聯代表明確的關聯性，可讓系統匯總邏輯裝置。
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: 'CIM_SystemDevice 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001653"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="dbf25-103">CIM_SystemDevice 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="dbf25-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dbf25-104">**CIM \_ SystemDevice** 關聯代表明確的關聯性，可讓系統匯總邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="dbf25-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbf25-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="dbf25-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbf25-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="dbf25-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbf25-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dbf25-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dbf25-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dbf25-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf25-109">語法</span><span class="sxs-lookup"><span data-stu-id="dbf25-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="dbf25-110">成員</span><span class="sxs-lookup"><span data-stu-id="dbf25-110">Members</span></span>

<span data-ttu-id="dbf25-111">**CIM \_ SystemDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dbf25-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="dbf25-112">屬性</span><span class="sxs-lookup"><span data-stu-id="dbf25-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbf25-113">屬性</span><span class="sxs-lookup"><span data-stu-id="dbf25-113">Properties</span></span>

<span data-ttu-id="dbf25-114">**CIM \_ SystemDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dbf25-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbf25-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dbf25-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf25-116">資料類型： **CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="dbf25-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="dbf25-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbf25-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf25-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="dbf25-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dbf25-119">在關聯中描述父系統的 [**CIM \_ 系統**](cim-system.md) 。</span><span class="sxs-lookup"><span data-stu-id="dbf25-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="dbf25-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dbf25-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf25-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="dbf25-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="dbf25-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dbf25-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf25-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="dbf25-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbf25-124">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述屬於系統元件的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="dbf25-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbf25-125">備註</span><span class="sxs-lookup"><span data-stu-id="dbf25-125">Remarks</span></span>

<span data-ttu-id="dbf25-126">**Cim \_ SystemDevice** 類別衍生自 [**cim \_ SystemComponent**](cim-systemcomponent.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf25-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="dbf25-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="dbf25-127">WMI does not implement this class.</span></span> <span data-ttu-id="dbf25-128">針對衍生自 **CIM \_ SYSTEMDEVICE** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf25-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dbf25-129">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="dbf25-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbf25-130">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dbf25-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf25-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbf25-131">Requirements</span></span>



| <span data-ttu-id="dbf25-132">需求</span><span class="sxs-lookup"><span data-stu-id="dbf25-132">Requirement</span></span> | <span data-ttu-id="dbf25-133">值</span><span class="sxs-lookup"><span data-stu-id="dbf25-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf25-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbf25-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf25-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbf25-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbf25-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbf25-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf25-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbf25-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbf25-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="dbf25-138">Namespace</span></span><br/>                | <span data-ttu-id="dbf25-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbf25-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbf25-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dbf25-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbf25-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbf25-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbf25-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf25-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbf25-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf25-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf25-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbf25-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf25-145">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="dbf25-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

