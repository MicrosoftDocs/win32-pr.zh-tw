---
description: Win32 \_ WMIElementSetting 關聯 WMI 類別會將 Windows 系統中執行的服務與它可以使用的 WMI 設定產生關聯。
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Win32_WMIElementSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847075"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="eb980-103">Win32 \_ WMIElementSetting 類別</span><span class="sxs-lookup"><span data-stu-id="eb980-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="eb980-104">**Win32 \_ WMIElementSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將 Windows 系統中執行的服務與它可以使用的 WMI 設定產生關聯。</span><span class="sxs-lookup"><span data-stu-id="eb980-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="eb980-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb980-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eb980-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="eb980-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb980-107">語法</span><span class="sxs-lookup"><span data-stu-id="eb980-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="eb980-108">成員</span><span class="sxs-lookup"><span data-stu-id="eb980-108">Members</span></span>

<span data-ttu-id="eb980-109">**Win32 \_ WMIElementSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb980-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="eb980-110">屬性</span><span class="sxs-lookup"><span data-stu-id="eb980-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb980-111">屬性</span><span class="sxs-lookup"><span data-stu-id="eb980-111">Properties</span></span>

<span data-ttu-id="eb980-112">**Win32 \_ WMIElementSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eb980-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb980-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb980-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb980-114">資料類型： **Win32 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="eb980-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="eb980-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb980-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb980-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Service" ) </span><span class="sxs-lookup"><span data-stu-id="eb980-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="eb980-117">使用或呈現 WMI 屬性之實例的參考，表示 Windows 服務。</span><span class="sxs-lookup"><span data-stu-id="eb980-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="eb980-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="eb980-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb980-119">資料類型： **Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="eb980-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="eb980-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb980-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb980-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ WMISetting" ) </span><span class="sxs-lookup"><span data-stu-id="eb980-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="eb980-122">代表 Windows 服務可用之 WMI 設定的實例參考。</span><span class="sxs-lookup"><span data-stu-id="eb980-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb980-123">備註</span><span class="sxs-lookup"><span data-stu-id="eb980-123">Remarks</span></span>

<span data-ttu-id="eb980-124">**Win32 \_ WMIElementSetting** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="eb980-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb980-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb980-125">Requirements</span></span>



| <span data-ttu-id="eb980-126">需求</span><span class="sxs-lookup"><span data-stu-id="eb980-126">Requirement</span></span> | <span data-ttu-id="eb980-127">值</span><span class="sxs-lookup"><span data-stu-id="eb980-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb980-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb980-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eb980-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb980-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb980-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb980-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eb980-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb980-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb980-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb980-132">Namespace</span></span><br/>                | <span data-ttu-id="eb980-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb980-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb980-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eb980-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb980-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb980-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb980-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eb980-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb980-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb980-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb980-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb980-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb980-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="eb980-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="eb980-140">WMI 服務管理類別</span><span class="sxs-lookup"><span data-stu-id="eb980-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
