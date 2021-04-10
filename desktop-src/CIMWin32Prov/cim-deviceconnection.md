---
description: CIM \_ DeviceConnection 關聯類別代表兩個或多個已連線的裝置。
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: 'CIM_DeviceConnection 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187763"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="71e9e-103">CIM_DeviceConnection 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="71e9e-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="71e9e-104">**CIM \_ DeviceConnection** 關聯類別代表兩個或多個已連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="71e9e-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71e9e-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="71e9e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="71e9e-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="71e9e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="71e9e-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="71e9e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="71e9e-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="71e9e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e9e-109">語法</span><span class="sxs-lookup"><span data-stu-id="71e9e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="71e9e-110">成員</span><span class="sxs-lookup"><span data-stu-id="71e9e-110">Members</span></span>

<span data-ttu-id="71e9e-111">**CIM \_ DeviceConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="71e9e-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="71e9e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="71e9e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71e9e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="71e9e-113">Properties</span></span>

<span data-ttu-id="71e9e-114">**CIM \_ DeviceConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="71e9e-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71e9e-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="71e9e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71e9e-116">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="71e9e-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71e9e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="71e9e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="71e9e-119">描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="71e9e-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="71e9e-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="71e9e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71e9e-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="71e9e-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71e9e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="71e9e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="71e9e-124">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述連接到前一個裝置的第二個邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="71e9e-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="71e9e-125">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="71e9e-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71e9e-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="71e9e-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71e9e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-128">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="71e9e-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="71e9e-129">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="71e9e-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="71e9e-130">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="71e9e-130">Data width is specified in bits.</span></span> <span data-ttu-id="71e9e-131">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="71e9e-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="71e9e-132">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="71e9e-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71e9e-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="71e9e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71e9e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-135">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="71e9e-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="71e9e-136">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="71e9e-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="71e9e-137">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="71e9e-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="71e9e-138">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="71e9e-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="71e9e-139">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="71e9e-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71e9e-140">備註</span><span class="sxs-lookup"><span data-stu-id="71e9e-140">Remarks</span></span>

<span data-ttu-id="71e9e-141">**Cim \_ DeviceConnection** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="71e9e-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="71e9e-142">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="71e9e-142">WMI does not implement this class.</span></span> <span data-ttu-id="71e9e-143">如需衍生自 **CIM \_ DeviceConnection** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="71e9e-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="71e9e-144">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="71e9e-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="71e9e-145">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9e-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e9e-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="71e9e-146">Requirements</span></span>



| <span data-ttu-id="71e9e-147">需求</span><span class="sxs-lookup"><span data-stu-id="71e9e-147">Requirement</span></span> | <span data-ttu-id="71e9e-148">值</span><span class="sxs-lookup"><span data-stu-id="71e9e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71e9e-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71e9e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="71e9e-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71e9e-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71e9e-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71e9e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="71e9e-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71e9e-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71e9e-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="71e9e-153">Namespace</span></span><br/>                | <span data-ttu-id="71e9e-154">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="71e9e-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71e9e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="71e9e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71e9e-156"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="71e9e-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71e9e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="71e9e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71e9e-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e9e-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e9e-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71e9e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e9e-160">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="71e9e-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

