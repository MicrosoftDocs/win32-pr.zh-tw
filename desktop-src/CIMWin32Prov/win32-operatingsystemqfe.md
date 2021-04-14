---
description: Win32 \_ OperatingSystemQFE 關聯 WMI 類別會將作業系統和套用的產品更新與 Win32 QuickFixEngineering 中的表示相關聯 \_ 。
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936450"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="19d14-103">Win32 \_ OperatingSystemQFE 類別</span><span class="sxs-lookup"><span data-stu-id="19d14-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="19d14-104">**Win32 \_ OperatingSystemQFE** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將作業系統和套用的產品更新與 [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)中的表示相關聯。</span><span class="sxs-lookup"><span data-stu-id="19d14-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="19d14-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="19d14-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="19d14-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="19d14-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d14-107">語法</span><span class="sxs-lookup"><span data-stu-id="19d14-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="19d14-108">成員</span><span class="sxs-lookup"><span data-stu-id="19d14-108">Members</span></span>

<span data-ttu-id="19d14-109">**Win32 \_ OperatingSystemQFE** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19d14-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="19d14-110">屬性</span><span class="sxs-lookup"><span data-stu-id="19d14-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19d14-111">屬性</span><span class="sxs-lookup"><span data-stu-id="19d14-111">Properties</span></span>

<span data-ttu-id="19d14-112">**Win32 \_ OperatingSystemQFE** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19d14-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19d14-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="19d14-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19d14-114">資料類型： **Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="19d14-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="19d14-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19d14-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19d14-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ 作業系統" ) </span><span class="sxs-lookup"><span data-stu-id="19d14-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="19d14-117">代表此關聯中的產品更新所影響之系統的實例參考。</span><span class="sxs-lookup"><span data-stu-id="19d14-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="19d14-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="19d14-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19d14-119">資料類型： **Win32 \_ QuickFixEngineering**</span><span class="sxs-lookup"><span data-stu-id="19d14-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="19d14-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19d14-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19d14-121">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**弱**](../wmisdk/standard-qualifiers.md)式、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「WMI \| Win32 QuickFixEngineering」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="19d14-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="19d14-122">代表在此關聯中套用至作業系統之物件實例的實例參考。</span><span class="sxs-lookup"><span data-stu-id="19d14-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19d14-123">備註</span><span class="sxs-lookup"><span data-stu-id="19d14-123">Remarks</span></span>

<span data-ttu-id="19d14-124">**Win32 \_ OperatingSystemQFE** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="19d14-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19d14-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="19d14-125">Requirements</span></span>



| <span data-ttu-id="19d14-126">需求</span><span class="sxs-lookup"><span data-stu-id="19d14-126">Requirement</span></span> | <span data-ttu-id="19d14-127">值</span><span class="sxs-lookup"><span data-stu-id="19d14-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d14-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19d14-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19d14-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19d14-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19d14-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19d14-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19d14-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19d14-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19d14-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="19d14-132">Namespace</span></span><br/>                | <span data-ttu-id="19d14-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19d14-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19d14-134">MOF</span><span class="sxs-lookup"><span data-stu-id="19d14-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19d14-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="19d14-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19d14-136">DLL</span><span class="sxs-lookup"><span data-stu-id="19d14-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d14-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d14-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d14-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19d14-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d14-139">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="19d14-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="19d14-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="19d14-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
