---
description: CIM \_ PackageAlarm 關聯代表將警示裝置安裝為套件一部分的關聯性。 此安裝指出封裝環境&\# 郵件、其安全性狀態或其整體健康情況的問題。
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: CIM_PackageAlarm 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110264"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="637da-104">CIM \_ PackageAlarm 類別</span><span class="sxs-lookup"><span data-stu-id="637da-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="637da-105">[**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum)關聯代表將警示裝置安裝為套件一部分的關聯性。</span><span class="sxs-lookup"><span data-stu-id="637da-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="637da-106">此安裝指出封裝的環境發生安全性狀態或其整體健康情況的問題。</span><span class="sxs-lookup"><span data-stu-id="637da-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="637da-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="637da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="637da-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="637da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="637da-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="637da-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="637da-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="637da-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="637da-111">語法</span><span class="sxs-lookup"><span data-stu-id="637da-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="637da-112">成員</span><span class="sxs-lookup"><span data-stu-id="637da-112">Members</span></span>

<span data-ttu-id="637da-113">**CIM \_ PackageAlarm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="637da-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="637da-114">屬性</span><span class="sxs-lookup"><span data-stu-id="637da-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="637da-115">屬性</span><span class="sxs-lookup"><span data-stu-id="637da-115">Properties</span></span>

<span data-ttu-id="637da-116">**CIM \_ PackageAlarm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="637da-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="637da-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="637da-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637da-118">資料類型： **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="637da-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="637da-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="637da-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637da-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="637da-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="637da-121">描述套件之警示裝置的 [**CIM \_ AlarmDevice**](cim-alarmdevice.md) 。</span><span class="sxs-lookup"><span data-stu-id="637da-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="637da-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="637da-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637da-123">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="637da-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="637da-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="637da-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637da-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="637da-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="637da-126">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述其健康情況、安全性、環境等的實體封裝是否有害怕。</span><span class="sxs-lookup"><span data-stu-id="637da-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="637da-127">備註</span><span class="sxs-lookup"><span data-stu-id="637da-127">Remarks</span></span>

<span data-ttu-id="637da-128">**CIM \_PackageAlarm** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="637da-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="637da-129">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="637da-129">WMI does not implement this class.</span></span>

<span data-ttu-id="637da-130">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="637da-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="637da-131">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="637da-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="637da-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="637da-132">Requirements</span></span>



| <span data-ttu-id="637da-133">需求</span><span class="sxs-lookup"><span data-stu-id="637da-133">Requirement</span></span> | <span data-ttu-id="637da-134">值</span><span class="sxs-lookup"><span data-stu-id="637da-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="637da-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="637da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="637da-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="637da-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="637da-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="637da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="637da-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="637da-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="637da-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="637da-139">Namespace</span></span><br/>                | <span data-ttu-id="637da-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="637da-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="637da-141">MOF</span><span class="sxs-lookup"><span data-stu-id="637da-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="637da-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="637da-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="637da-143">DLL</span><span class="sxs-lookup"><span data-stu-id="637da-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637da-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="637da-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637da-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="637da-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637da-146">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="637da-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

