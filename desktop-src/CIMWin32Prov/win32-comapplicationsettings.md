---
description: Win32 \_ COMApplicationSettings 關聯 WMI 類別會關聯 DCOM 應用程式及其設定。
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Win32_COMApplicationSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187622"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="54932-103">Win32 \_ COMApplicationSettings 類別</span><span class="sxs-lookup"><span data-stu-id="54932-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="54932-104">**Win32 \_ COMApplicationSettings** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯 DCOM 應用程式及其設定。</span><span class="sxs-lookup"><span data-stu-id="54932-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="54932-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="54932-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="54932-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="54932-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54932-107">語法</span><span class="sxs-lookup"><span data-stu-id="54932-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="54932-108">成員</span><span class="sxs-lookup"><span data-stu-id="54932-108">Members</span></span>

<span data-ttu-id="54932-109">**Win32 \_ COMApplicationSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="54932-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="54932-110">屬性</span><span class="sxs-lookup"><span data-stu-id="54932-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54932-111">屬性</span><span class="sxs-lookup"><span data-stu-id="54932-111">Properties</span></span>

<span data-ttu-id="54932-112">**Win32 \_ COMApplicationSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="54932-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54932-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="54932-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54932-114">資料類型： **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="54932-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="54932-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="54932-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54932-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DCOMApplication" ) </span><span class="sxs-lookup"><span data-stu-id="54932-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="54932-117">[**Win32 \_ DCOMApplication**](win32-dcomapplication.md) ，代表套用設定的 DCOM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="54932-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="54932-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="54932-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54932-119">資料類型： **Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="54932-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="54932-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="54932-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54932-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "設定" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DCOMApplicationSetting" ) </span><span class="sxs-lookup"><span data-stu-id="54932-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="54932-122">[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md) ，表示與 DCOM 應用程式相關聯的設定。</span><span class="sxs-lookup"><span data-stu-id="54932-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54932-123">備註</span><span class="sxs-lookup"><span data-stu-id="54932-123">Remarks</span></span>

<span data-ttu-id="54932-124">**Win32 \_ COMApplicationSettings** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="54932-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54932-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="54932-125">Requirements</span></span>



| <span data-ttu-id="54932-126">需求</span><span class="sxs-lookup"><span data-stu-id="54932-126">Requirement</span></span> | <span data-ttu-id="54932-127">值</span><span class="sxs-lookup"><span data-stu-id="54932-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54932-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54932-128">Minimum supported client</span></span><br/> | <span data-ttu-id="54932-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54932-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54932-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54932-130">Minimum supported server</span></span><br/> | <span data-ttu-id="54932-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54932-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54932-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="54932-132">Namespace</span></span><br/>                | <span data-ttu-id="54932-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="54932-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54932-134">MOF</span><span class="sxs-lookup"><span data-stu-id="54932-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54932-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="54932-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54932-136">DLL</span><span class="sxs-lookup"><span data-stu-id="54932-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54932-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54932-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54932-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54932-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54932-139">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="54932-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="54932-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54932-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

