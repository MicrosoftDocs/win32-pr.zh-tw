---
description: Win32 \_ SystemDriverPNPEntity 關聯 WMI 類別會將執行 Windows 的電腦系統上的隨插即用裝置與支援隨插即用裝置的驅動程式產生關聯。
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510582"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="e8d64-103">Win32 \_ SystemDriverPNPEntity 類別</span><span class="sxs-lookup"><span data-stu-id="e8d64-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="e8d64-104">**Win32 \_ SystemDriverPNPEntity** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將執行 Windows 的電腦系統上的隨插即用裝置與支援隨插即用裝置的驅動程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e8d64-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="e8d64-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8d64-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e8d64-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e8d64-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d64-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8d64-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e8d64-108">成員</span><span class="sxs-lookup"><span data-stu-id="e8d64-108">Members</span></span>

<span data-ttu-id="e8d64-109">**Win32 \_ SystemDriverPNPEntity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e8d64-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="e8d64-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e8d64-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8d64-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e8d64-111">Properties</span></span>

<span data-ttu-id="e8d64-112">**Win32 \_ SystemDriverPNPEntity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e8d64-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8d64-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="e8d64-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d64-114">資料類型： **Win32 \_ PNPEntity**</span><span class="sxs-lookup"><span data-stu-id="e8d64-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="e8d64-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8d64-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d64-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PNPEntity" ) </span><span class="sxs-lookup"><span data-stu-id="e8d64-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="e8d64-117">代表驅動程式所控制的隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="e8d64-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="e8d64-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e8d64-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d64-119">資料類型： **Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="e8d64-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="e8d64-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8d64-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d64-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「WMI \| Win32 >systemdriver」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="e8d64-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="e8d64-122">[**Win32 \_ >systemdriver**](win32-systemdriver.md) ，表示支援隨插即用裝置的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e8d64-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8d64-123">備註</span><span class="sxs-lookup"><span data-stu-id="e8d64-123">Remarks</span></span>

<span data-ttu-id="e8d64-124">**Win32 \_ SystemDriverPNPEntity** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="e8d64-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d64-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8d64-125">Requirements</span></span>



| <span data-ttu-id="e8d64-126">需求</span><span class="sxs-lookup"><span data-stu-id="e8d64-126">Requirement</span></span> | <span data-ttu-id="e8d64-127">值</span><span class="sxs-lookup"><span data-stu-id="e8d64-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d64-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8d64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d64-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8d64-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8d64-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8d64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d64-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8d64-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8d64-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="e8d64-132">Namespace</span></span><br/>                | <span data-ttu-id="e8d64-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e8d64-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8d64-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e8d64-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8d64-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8d64-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8d64-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8d64-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8d64-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8d64-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8d64-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8d64-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d64-139">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="e8d64-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="e8d64-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e8d64-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
