---
description: Win32 \_ SystemSetting 抽象關聯 WMI 類別會關聯電腦系統和該系統上的一般設定。
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468533"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="b43ba-103">Win32 \_ SystemSetting 類別</span><span class="sxs-lookup"><span data-stu-id="b43ba-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="b43ba-104">**Win32 \_ SystemSetting** 抽象關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會關聯電腦系統和該系統上的一般設定。</span><span class="sxs-lookup"><span data-stu-id="b43ba-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="b43ba-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b43ba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b43ba-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b43ba-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43ba-107">語法</span><span class="sxs-lookup"><span data-stu-id="b43ba-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="b43ba-108">成員</span><span class="sxs-lookup"><span data-stu-id="b43ba-108">Members</span></span>

<span data-ttu-id="b43ba-109">**Win32 \_ SystemSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b43ba-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="b43ba-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b43ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b43ba-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b43ba-111">Properties</span></span>

<span data-ttu-id="b43ba-112">**Win32 \_ SystemSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b43ba-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b43ba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b43ba-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ba-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="b43ba-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b43ba-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b43ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ba-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="b43ba-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b43ba-117">代表可套用此設定之電腦系統屬性的實例參考。</span><span class="sxs-lookup"><span data-stu-id="b43ba-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="b43ba-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="b43ba-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ba-119">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="b43ba-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="b43ba-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b43ba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ba-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「設定」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| cim 設定」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="b43ba-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="b43ba-122">實例的參考，代表可以套用至電腦系統之設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="b43ba-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b43ba-123">備註</span><span class="sxs-lookup"><span data-stu-id="b43ba-123">Remarks</span></span>

<span data-ttu-id="b43ba-124">**Win32 \_ SystemSetting** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="b43ba-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b43ba-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b43ba-125">Requirements</span></span>



| <span data-ttu-id="b43ba-126">需求</span><span class="sxs-lookup"><span data-stu-id="b43ba-126">Requirement</span></span> | <span data-ttu-id="b43ba-127">值</span><span class="sxs-lookup"><span data-stu-id="b43ba-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b43ba-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b43ba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b43ba-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b43ba-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b43ba-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b43ba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b43ba-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b43ba-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b43ba-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="b43ba-132">Namespace</span></span><br/>                | <span data-ttu-id="b43ba-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b43ba-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b43ba-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b43ba-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b43ba-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b43ba-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b43ba-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b43ba-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b43ba-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b43ba-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b43ba-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b43ba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43ba-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="b43ba-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="b43ba-140">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b43ba-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
