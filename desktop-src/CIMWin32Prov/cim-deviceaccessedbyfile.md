---
description: CIM \_ DeviceAccessedByFile 關聯類別會使用參考的 CIM DeviceFile 類別來指定存取的邏輯裝置 \_ 。
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847366"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="fb8ff-103">CIM \_ DeviceAccessedByFile 類別</span><span class="sxs-lookup"><span data-stu-id="fb8ff-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="fb8ff-104">**CIM \_ DeviceAccessedByFile** 關聯類別會使用參考的 [**CIM \_ DeviceFile**](cim-devicefile.md)類別來指定存取的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb8ff-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb8ff-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb8ff-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb8ff-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8ff-109">語法</span><span class="sxs-lookup"><span data-stu-id="fb8ff-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fb8ff-110">成員</span><span class="sxs-lookup"><span data-stu-id="fb8ff-110">Members</span></span>

<span data-ttu-id="fb8ff-111">**CIM \_ DeviceAccessedByFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fb8ff-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="fb8ff-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fb8ff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb8ff-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fb8ff-113">Properties</span></span>

<span data-ttu-id="fb8ff-114">**CIM \_ DeviceAccessedByFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb8ff-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8ff-116">資料類型： **CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="fb8ff-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb8ff-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb8ff-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="fb8ff-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fb8ff-119">描述裝置檔案的 [**CIM \_ DeviceFile**](cim-devicefile.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="fb8ff-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb8ff-121">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="fb8ff-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fb8ff-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb8ff-123">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="fb8ff-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fb8ff-124">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述使用裝置檔案所存取的裝置。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb8ff-125">備註</span><span class="sxs-lookup"><span data-stu-id="fb8ff-125">Remarks</span></span>

<span data-ttu-id="fb8ff-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-126">WMI does not implement this class.</span></span>

<span data-ttu-id="fb8ff-127">**Cim \_ DeviceAccessedByFile** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fb8ff-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb8ff-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fb8ff-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8ff-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb8ff-130">Requirements</span></span>



| <span data-ttu-id="fb8ff-131">需求</span><span class="sxs-lookup"><span data-stu-id="fb8ff-131">Requirement</span></span> | <span data-ttu-id="fb8ff-132">值</span><span class="sxs-lookup"><span data-stu-id="fb8ff-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb8ff-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb8ff-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fb8ff-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb8ff-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb8ff-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb8ff-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fb8ff-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb8ff-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb8ff-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="fb8ff-137">Namespace</span></span><br/>                | <span data-ttu-id="fb8ff-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb8ff-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb8ff-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fb8ff-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb8ff-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb8ff-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb8ff-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fb8ff-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb8ff-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb8ff-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb8ff-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb8ff-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8ff-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="fb8ff-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

