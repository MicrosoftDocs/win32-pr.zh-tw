---
description: Win32 \_ DeviceSettings abstract、ASSOCIATION WMI 類別會將邏輯裝置和可以套用的設定產生關聯。
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Win32_DeviceSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190991"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="e7ae7-103">Win32 \_ DeviceSettings 類別</span><span class="sxs-lookup"><span data-stu-id="e7ae7-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="e7ae7-104">**Win32 \_ DeviceSettings** Abstract、association [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將邏輯裝置和可以套用的設定產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="e7ae7-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e7ae7-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ae7-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7ae7-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="e7ae7-108">成員</span><span class="sxs-lookup"><span data-stu-id="e7ae7-108">Members</span></span>

<span data-ttu-id="e7ae7-109">**Win32 \_ DeviceSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e7ae7-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e7ae7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e7ae7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7ae7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e7ae7-111">Properties</span></span>

<span data-ttu-id="e7ae7-112">**Win32 \_ DeviceSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7ae7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7ae7-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ae7-114">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e7ae7-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e7ae7-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7ae7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ae7-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \| CIM \_ LogicalDevice" ) </span><span class="sxs-lookup"><span data-stu-id="e7ae7-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="e7ae7-117">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，代表可套用設定的邏輯裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e7ae7-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="e7ae7-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ae7-119">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="e7ae7-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="e7ae7-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7ae7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ae7-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「設定」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim 設定」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="e7ae7-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="e7ae7-122">[**CIM \_ 設定**](cim-setting.md)，代表可以套用至邏輯裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ae7-123">備註</span><span class="sxs-lookup"><span data-stu-id="e7ae7-123">Remarks</span></span>

<span data-ttu-id="e7ae7-124">**Win32 \_ DeviceSettings** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="e7ae7-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ae7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7ae7-125">Requirements</span></span>



| <span data-ttu-id="e7ae7-126">需求</span><span class="sxs-lookup"><span data-stu-id="e7ae7-126">Requirement</span></span> | <span data-ttu-id="e7ae7-127">值</span><span class="sxs-lookup"><span data-stu-id="e7ae7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ae7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7ae7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ae7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7ae7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7ae7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7ae7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ae7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7ae7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7ae7-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="e7ae7-132">Namespace</span></span><br/>                | <span data-ttu-id="e7ae7-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7ae7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7ae7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e7ae7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7ae7-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7ae7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7ae7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e7ae7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7ae7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7ae7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ae7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7ae7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ae7-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="e7ae7-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e7ae7-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e7ae7-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

